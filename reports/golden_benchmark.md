# Lab 17 Golden Set Report

- Implementation: `student`
- Kind: `golden`
- Cases: **20**
- Passed: **20/20**
- Evidence hit rate: **100.0%**
- Average retrieval latency: **1126.0 ms**
- Average token reduction vs full source context: **4.5%**
- Golden bonus: **10/10** (100% required)

| Case | Layer | Pass | Latency ms | Retrieved tokens | Token reduction | Missing / Error |
| --- | --- | --- | ---: | ---: | ---: | --- |
| G01 | short_term | PASS | 0.6 | 227 | 0.0% |  |
| G02 | short_term | PASS | 0.1 | 133 | 0.0% |  |
| G06 | long_term | PASS | 1596.9 | 495 | 0.0% |  |
| G09 | semantic | PASS | 244.0 | 406 | 11.6% |  |
| G10 | semantic | PASS | 382.4 | 262 | 42.9% |  |
| G14 | mixed | PASS | 1725.5 | 581 | 0.0% |  |
| G03 | long_term | PASS | 1631.3 | 1020 | 0.0% |  |
| G04 | long_term | PASS | 1655.5 | 945 | 0.0% |  |
| G07 | episodic | PASS | 265.6 | 564 | 0.0% |  |
| G08 | episodic | PASS | 263.6 | 578 | 0.0% |  |
| G11 | mixed | PASS | 1973.8 | 581 | 0.0% |  |
| G13 | mixed | PASS | 484.6 | 500 | 11.5% |  |
| G15 | mixed | PASS | 1785.4 | 831 | 0.0% |  |
| G16 | mixed | PASS | 1667.9 | 581 | 0.0% |  |
| G17 | mixed | PASS | 1780.1 | 581 | 0.0% |  |
| G18 | mixed | PASS | 490.9 | 500 | 11.5% |  |
| G19 | mixed | PASS | 1523.9 | 581 | 0.0% |  |
| G05 | long_term | PASS | 1352.5 | 1091 | 0.0% |  |
| G12 | mixed | PASS | 1715.5 | 555 | 12.2% |  |
| G20 | mixed | PASS | 1979.4 | 756 | 0.0% |  |

## Evidence excerpts

### G01 - short_term

`<SESSION_SUMMARY> user: Constraint HOLD-ALPHA-0900: standup is 09:00 sharp and must not be forgotten. | assistant: Noted standup constraint. | user: Constraint HOLD-BETA-STAGING: writes go to staging DB only. | assistant: Noted staging constraint. | user: Filler A about button padding. | assistant: Filler A. | user: Filler B about color tokens. | assistant: Filler B. | user: Filler C about copy tone. | assistant: Filler C. </SESSION_SUMMARY> <DURABLE_NOTES> - user: Constraint HOLD-ALPHA-0900: standup is 09:00 sharp and must not be forgotten. - assistant: Noted standup constraint. - user: Constraint HOLD-BETA-STAGING: writes go to staging DB only. - assistant: Noted staging constraint. </DURA`

### G02 - short_term

`<RECENT_TURNS> user: Ten du an ca nhan cua toi la ORCHID-27. Toi thich Python va khong thich Java. Khi giai thich code, hay dung vi du ngan. assistant: Da hieu: demo ca nhan ORCHID-27, uu tien Python, tranh Java, vi du ngan. user: Toi dang hoc async/await va hay nham coroutine voi Task. Neu sau nay gap chu de nay, hay giai thich bang timeline. assistant: Toi se uu tien timeline khi giai thich coroutine va Task. user: TODO: hoan thanh benchmark report truoc thu Sau luc 16:00. Day la open loop LAB-REPORT-1600. </RECENT_TURNS>`

### G06 - long_term

`}: Toi la Lan. Du an cua toi la LOTUS-88. Toi uu tien Java va Spring Boot, va khong dung Python trong vi du backend. }: Minh la Lan, phap ly hoi gat truoc khi bat memory tren san pham. Viet hop dong ngan: backend minh dang dung ngon ngu/framework nao, va quy tac luu/xoa bo nho ca nhan trong lab yeu cau opt-in va verify ra sao? Chi stack cua Lan. The user's project is LOTUS-88. They prioritize Java and Spring Boot for backend development and do not use Python. Content: Lab Assistant (assistant): Da hieu: LOTUS-88, Java + Spring Boot cho backend examples. - LOTUS-88 uses Java + Spring Boot for backend examples. (2026-08-01 11:00:20) Summary: Da hieu uses Java + Spring Boot for backend examples`

### G09 - semantic

`EPISODE: For POST /payments, every retryable request MUST send the same Idempotency-Key. Retry only HTTP 429 or transient 5xx errors, use exponential-backoff, and stop after max-3-retries. Marker: PAYMENT-RULE-3. EPISODE: {"id":"kb-payment-retry","entity":"Payment API Retry Policy","summary":"For POST /payments, every retryable request MUST send the same Idempotency-Key. Retry only HTTP 429 or transient 5xx errors, use exponential-backoff, and stop after max-3-retries. Marker: PAYMENT-RULE-3.","source":"internal-api-guideline-v3","updated_at":"2026-08-10T00:00:00Z"} EPISODE: Do not persist personal data without explicit opt-in. A deletion request must remove user-scoped memory and be verifie`

### G10 - semantic

`EPISODE: Reserve bounded context for memory. This lab uses short-term 10 percent, long-term 4 percent, episodic 3 percent, semantic 3 percent; trim lower-priority memory first. Marker: BUDGET-10-4-3-3. EPISODE: Do not persist personal data without explicit opt-in. A deletion request must remove user-scoped memory and be verified across every store. Marker: DELETE-VERIFY-ALL. EPISODE: {"id":"kb-memory-privacy","entity":"Agent Memory Privacy Rule","summary":"Do not persist personal data without explicit opt-in. A deletion request must remove user-scoped memory and be verified across every store. Marker: DELETE-VERIFY-ALL.","source":"memory-governance-policy","updated_at":"2026-08-12T00:00:00Z"`

### G14 - mixed

`<LONG_TERM> }: Toi la Lan. Du an cua toi la LOTUS-88. Toi uu tien Java va Spring Boot, va khong dung Python trong vi du backend. }: Lan uu tien stack backend nao cho LOTUS-88? The user's project is LOTUS-88. They prioritize Java and Spring Boot for backend development and do not use Python. Content: Lab Assistant (assistant): Da hieu: LOTUS-88, Java + Spring Boot cho backend examples. - LOTUS-88 uses Java + Spring Boot for backend examples. (2026-08-01 11:00:20) Summary: Da hieu uses Java + Spring Boot for backend examples, specifically for LOTUS-88. Summary: The user's project is LOTUS-88. They prioritize Java and Spring Boot for backend development and do not use Python. - Lan Tran is work`

### G03 - long_term

`}: Voi demo ca nhan cua Minh, ngon ngu uu tien la gi? - Minh Nguyen uses Python for personal demos on ORCHID-27. (2026-08-05 08:00:00) - Minh Nguyen's personal project is ORCHID-27. (2026-08-01 09:00:00) - Minh Nguyen still prefers Python for personal demos. (2026-08-05 08:00:00) FACT: ORCHID-27 prioritizes Python. [valid_at=2026-08-01T09:00:20Z, invalid_at=2026-08-05T08:00:00Z] Minh prefers Python and dislikes Java. For code explanations, Minh wants short examples. Minh is learning async/await and often confuses coroutines with Tasks, wanting timeline-based explanations for these topics. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS; Python is not to be us`

### G04 - long_term

`}: Minh con mot open-loop phai nop truoc deadline, dong thoi muon ghi chu retry payment dung so lan toi da theo policy. Nac lai ma task/deadline con dang do, va gioi han retry chinh thuc trong lab. Summary: Minh Nguyen needs to complete the benchmark report before Friday at 16:00. This is an open-loop report designated as LAB-REPORT-1600. - Minh Nguyen uses Python for personal demos on ORCHID-27. (2026-08-05 08:00:00) - Minh Nguyen's personal project is ORCHID-27. (2026-08-01 09:00:00) - Minh Nguyen is learning about Task. (2026-08-01 09:02:00) - Minh Nguyen often confuses coroutine with Task. (2026-08-01 09:02:00) - ORCHID-27 prioritizes Python. (2026-08-01 09:00:20) - ORCHID-27 avoids Java`

### G07 - episodic

`EPISODE: Cach hieu qua la reuse aiohttp ClientSession va dat concurrency=20. Reflection: loi chinh la connection churn, khong phai timeout threshold. Ma su co ASYNC-FIX-20. EPISODE: Hom nay toi debug async HTTP. Toi da thu tang timeout len 60s nhung van fail. EPISODE: Da ghi nhan trajectory: increase timeout khong hieu qua; ClientSession + concurrency=20 giai quyet connection churn. EPISODE: Ten du an ca nhan cua toi la ORCHID-27. Toi thich Python va khong thich Java. Khi giai thich code, hay dung vi du ngan. EPISODE: Chuan bi demo ca nhan: ten/ma project rieng cua Minh la gi, va lan async HTTP truoc minh reuse client nhu the nao (kem ma su co)? Khong can policy domain chung, chi memory cua `

### G08 - episodic

`EPISODE: Da tach scope: BLUEBIRD-42 dung TypeScript/NestJS; ORCHID-27 van uu tien Python. EPISODE: Cach hieu qua la reuse aiohttp ClientSession va dat concurrency=20. Reflection: loi chinh la connection churn, khong phai timeout threshold. Ma su co ASYNC-FIX-20. EPISODE: Minh sap viet script ca nhan de tai hien su co latency, muon code dung ngon ngu minh thich khi lam mot minh, dong thoi bam sat playbook incident cua lab chu dung vo tang timeout. G EPISODE: Ten du an ca nhan cua toi la ORCHID-27. Toi thich Python va khong thich Java. Khi giai thich code, hay dung vi du ngan. EPISODE: Toi nay minh viet tool ca nhan de tai hien su co HTTP roi sua dung playbook. Can ba manh: ngon ngu minh thich`

### G11 - mixed

`<LONG_TERM> }: Toi nay minh viet tool ca nhan de tai hien su co HTTP roi sua dung playbook. Can ba manh: ngon ngu minh thich khi lam mot minh, ma su co async lan truoc, va buoc playbook truoc khi tang timeout. Scope Minh, dung tron Lan. FACT: Minh Nguyen's personal project is ORCHID-27. [valid_at=2026-08-01T09:00:00Z, invalid_at=None] FACT: Minh Nguyen uses Python for personal demos on ORCHID-27. [valid_at=2026-08-05T08:00:00Z, invalid_at=None] FACT: The incident ASYNC-FIX-20 addresses the issue of connection churn. [valid_at=2026-08-03T10:03:00Z, invalid_at=None] Minh's personal project is named ORCHID-27, for which Minh prefers Python. For the company project BLUEBIRD-42, the backend must `

### G13 - mixed

`<EPISODIC> EPISODE: Da tach scope: BLUEBIRD-42 dung TypeScript/NestJS; ORCHID-27 van uu tien Python. EPISODE: Minh con mot open-loop phai nop truoc deadline, dong thoi muon ghi chu retry payment dung so lan toi da theo policy. Nac lai ma task/deadline con dang do, va gioi han retry chinh t EPISODE: Toi nay minh viet tool ca nhan de tai hien su co HTTP roi sua dung playbook. Can ba manh: ngon ngu minh thich khi lam mot minh, ma su co async lan truoc, va buoc playbook truoc khi EPISODE: Minh sap giai thich coroutine cho ban, dong thoi can nhac policy retry payment vao vi du. Minh hoc kieu nao thi de nho? Va request retry payment phai mang header nao? Dung lay styl EPISODE: Chuan bi demo ca nha`

### G15 - mixed

`<LONG_TERM> Summary: Minh Nguyen was debugging async HTTP. Minh tried increasing the timeout to 60 seconds, but it still failed. }: Chuan bi demo ca nhan: ten/ma project rieng cua Minh la gi, va lan async HTTP truoc minh reuse client nhu the nao (kem ma su co)? Khong can policy domain chung, chi memory cua Minh. - Minh Nguyen uses Python for personal demos on ORCHID-27. (2026-08-05 08:00:00) - Minh Nguyen's personal project is ORCHID-27. (2026-08-01 09:00:00) - The async HTTP debugging still fails even after increasing the timeout to 60s. (2026-08-03 10:00:00) - Minh Nguyen is debugging async HTTP. (2026-08-03 10:00:00) FACT: The incident ASYNC-FIX-20 addresses the issue of connection churn.`

### G16 - mixed

`<LONG_TERM> }: Mai hop mentor, toi nay minh muon don open-loop. Liet ke viec chua dong, deadline, va ma dinh danh task. Can du ba manh de ghi vao note hop. Summary: Minh Nguyen needs to complete the benchmark report before Friday at 16:00. This is an open-loop report designated as LAB-REPORT-1600. - Minh Nguyen uses Python for personal demos on ORCHID-27. (2026-08-05 08:00:00) - Minh Nguyen's personal project is ORCHID-27. (2026-08-01 09:00:00) - Minh Nguyen is learning about Task. (2026-08-01 09:02:00) - Minh Nguyen often confuses coroutine with Task. (2026-08-01 09:02:00) - ORCHID-27 prioritizes Python. (2026-08-01 09:00:20) FACT: The benchmark report is identified as LAB-REPORT-1600. [val`

### G17 - mixed

`<LONG_TERM> }: Hay chon huong dan code retry payment phu hop voi preference ca nhan cua Minh. - Minh Nguyen uses Python for personal demos on ORCHID-27. (2026-08-05 08:00:00) - Minh Nguyen's personal project is ORCHID-27. (2026-08-01 09:00:00) Summary: Minh Nguyen is learning async/await and often confuses coroutine with Task. Minh requested an explanation of this topic via a timeline if it arises later. - Minh Nguyen is learning about coroutine. (2026-08-01 09:02:00) - Minh Nguyen often confuses coroutine with Task. (2026-08-01 09:02:00) - ORCHID-27 prioritizes Python. (2026-08-01 09:00:20) - ORCHID-27 avoids Java. (2026-08-01 09:00:20) Minh's personal project is named ORCHID-27, for which `

### G18 - mixed

`<EPISODIC> EPISODE: Ten du an ca nhan cua toi la ORCHID-27. Toi thich Python va khong thich Java. Khi giai thich code, hay dung vi du ngan. EPISODE: Cach hieu qua la reuse aiohttp ClientSession va dat concurrency=20. Reflection: loi chinh la connection churn, khong phai timeout threshold. Ma su co ASYNC-FIX-20. EPISODE: Cong ty yeu cau chinh context window cho agent tren dung backend du an cong ty. Minh can biet stack bat buoc cua BLUEBIRD va ty le budget bon tang nho trong lab de cau hinh cho dun EPISODE: Da hieu: demo ca nhan ORCHID-27, uu tien Python, tranh Java, vi du ngan. EPISODE: TODO: hoan thanh benchmark report truoc thu Sau luc 16:00. Day la open loop LAB-REPORT-1600. EPISODE: Cap `

### G19 - mixed

`<LONG_TERM> - Minh Nguyen uses Python for personal demos on ORCHID-27. (2026-08-05 08:00:00) - Minh Nguyen's personal project is ORCHID-27. (2026-08-01 09:00:00) FACT: Minh Nguyen is debugging async HTTP. [valid_at=2026-08-03T10:00:00Z, invalid_at=None] FACT: The incident ASYNC-FIX-20 addresses the issue of connection churn. [valid_at=2026-08-03T10:03:00Z, invalid_at=None] FACT: For the company project BLUEBIRD-42, NestJS is required for the backend. [valid_at=2026-08-05T08:00:00Z, invalid_at=None] Minh's personal project is named ORCHID-27, for which Minh prefers Python. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS. Minh needs to complete the benchmark re`

### G05 - long_term

`}: Cap nhat moi: voi du an cong ty BLUEBIRD-42, backend bat buoc dung TypeScript voi NestJS; khong dung Python cho backend du an nay. Preference Python van dung cho demo ca nhan ORCHID-27. FACT: Python is not to be used for the backend of the company project BLUEBIRD-42. [valid_at=2026-08-05T08:00:00Z, invalid_at=None] - Minh Nguyen uses Python for personal demos on ORCHID-27. (2026-08-05 08:00:00) - Minh Nguyen's personal project is ORCHID-27. (2026-08-01 09:00:00) FACT: For the company project BLUEBIRD-42, NestJS is required for the backend. [valid_at=2026-08-05T08:00:00Z, invalid_at=None] FACT: For the company project BLUEBIRD-42, TypeScript is required for the backend. [valid_at=2026-08-`

### G12 - mixed

`<LONG_TERM> }: Backend cua BLUEBIRD-42 bat buoc dung stack gi? FACT: For the company project BLUEBIRD-42, NestJS is required for the backend. [valid_at=2026-08-05T08:00:00Z, invalid_at=None] FACT: For the company project BLUEBIRD-42, TypeScript is required for the backend. [valid_at=2026-08-05T08:00:00Z, invalid_at=None] FACT: Python is not to be used for the backend of the company project BLUEBIRD-42. [valid_at=2026-08-05T08:00:00Z, invalid_at=None] - Minh Nguyen's personal project is ORCHID-27. (2026-08-01 09:00:00) - Minh Nguyen uses Python for personal demos on ORCHID-27. (2026-08-05 08:00:00) Minh's personal project is named ORCHID-27, for which Minh prefers Python. For the company proj`

### G20 - mixed

`<SHORT_TERM> <SESSION_SUMMARY> user: Constraint HOLD-ALPHA-0900: standup is 09:00 sharp and must not be forgotten. | assistant: Noted standup constraint. | user: Filler about dashboard widgets. | assistant: Filler. | user: Filler about CSS variables. | assistant: Filler. | user: Filler about copy review. | assistant: Filler. </SESSION_SUMMARY> <DURABLE_NOTES> - user: Constraint HOLD-ALPHA-0900: standup is 09:00 sharp and must not be forgotten. - assistant: Noted standup constraint. </DURABLE_NOTES> <RECENT_TURNS> user: Filler about empty charts. assistant: Filler. user: Filler about telemetry. assistant: Filler. user: Filler about a11y labels. assistant: Filler. </RECENT_TURNS> </SHORT_TERM>`
