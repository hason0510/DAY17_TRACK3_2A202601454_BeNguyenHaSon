# Lab 17 — Multi-Memory Agent voi Zep

**Ket qua:** student 11/11 (100%), no-memory 2/11 (18.2%), golden 20/20, `pytest` pass. Chi
tiet trong `reports/`.

## 3 cau thuc hanh

**1. Layer quan trong nhat: long_term.** Chiem 4/11 case (E02, E03, E08, E09 = 20/56 diem),
la layer duy nhat vua vuot ranh gioi session vua giu isolation 2 user; mat no thi E07 cung
mat `Python`.

**2. Trade-off Zep vs Redis+Qdrant.** Zep cho san extraction fact/episode, temporal validity
(`valid_at`/`invalid_at`) va scoping theo `user_id`, nen E08 recency va E09 isolation gan nhu
mien phi; doi lai latency long_term ~1.5s moi call (E09 co luc 5.5s), phu thuoc vendor va
ingestion bat dong bo (phai poll truoc khi search). Redis+Qdrant nhanh milisecond va tu chu
du lieu, nhung phai tu viet extraction, conflict resolution, scoping, TTL — phan ton cong nhat.

**3. Guardrail chong memory poisoning.** (a) `prime_eval_thread` dung
`ignore_roles=["user"]` nen query danh gia khong bi ghi thanh durable fact: input khong tu
dong tro thanh memory. (b) `privacy_guard` bat consent opt-in va `minimize_pii` truoc moi
ingest. (c) Heartbeat chi dedupe / danh dau stale / tao recap, **khong** tu them instruction
hay quyen moi; preference change high-impact can policy review (`AGENTS.md`).
(d) Durable record giu source/timestamp/confidence de truy vet.

## 4 cau phan tich benchmark

**1. Hit rate thap nhat:** student run khong layer nao thap, moi layer 100%. Baseline
no-memory: moi layer durable 0% (long_term 0/4, episodic 0/2, semantic 0/2, mixed 0/1), chi
short_term 2/2 vi evidence con trong thread hien tai.

**2. Query nhieu token nhat:** E02 = 1401 token, roi E03 (1395), E08 (1389) — deu long_term:
Context Block cong edges search `limit=20` tra ca summary lan fact list.

**3. E07 (mixed) = long_term + semantic.** Evidence bat buoc: `Python` (preference ca nhan)
va `Idempotency-Key` (PAYMENT-RULE-3, KB dung chung). Budget cat long_term 1390 -> 324 token
(limit 320) ma van giu `Python`; semantic 148 token vua limit 240.

**4. Token reduction:** memory 14.2% vs no-memory 81.8%. No-memory "tiet kiem" hon chi vi
retrieve rong: reduction cao nhung hit rate 18.2%. Reduction chi co nghia khi doc kem hit
rate.

## E08 recency va E10 compaction

**E08:** stage 3 them constraint scoped BLUEBIRD-42 -> TypeScript/NestJS ma khong xoa
preference Python cua ORCHID-27 (conflict rule "recency + scope"), nen E02 va E08 PASS dong
thoi.

**E10:** o `max_recent_messages=4`, turn chua `REVIEW-DEADLINE-1600` bi evict khoi
`<RECENT_TURNS>` nhung `extract_durable_notes` nang no len `<DURABLE_NOTES>`, nen `Friday` va
`16:00` van retrieve duoc. Buffer khong du vi khong phan biet constraint voi filler.
