# Lab 17 Benchmark Report

- Implementation: `student`
- Kind: `practice`
- Cases: **11**
- Passed: **11/11**
- Evidence hit rate: **100.0%**
- Average retrieval latency: **842.5 ms**
- Average token reduction vs full source context: **14.3%**

| Case | Layer | Pass | Latency ms | Retrieved tokens | Token reduction | Missing / Error |
| --- | --- | --- | ---: | ---: | ---: | --- |
| E01 | short_term | PASS | 0.1 | 133 | 0.0% |  |
| E06 | semantic | PASS | 455.2 | 146 | 68.2% |  |
| E09 | long_term | PASS | 1683.3 | 481 | 0.0% |  |
| E10 | short_term | PASS | 0.5 | 195 | 0.0% |  |
| E02 | long_term | PASS | 1424.4 | 1082 | 0.0% |  |
| E03 | long_term | PASS | 1446.4 | 911 | 0.0% |  |
| E04 | episodic | PASS | 462.3 | 580 | 0.0% |  |
| E05 | episodic | PASS | 317.1 | 597 | 0.0% |  |
| E07 | mixed | PASS | 1856.8 | 482 | 14.7% |  |
| E11 | semantic | PASS | 258.0 | 143 | 74.7% |  |
| E08 | long_term | PASS | 1363.1 | 1028 | 0.0% |  |

## Evidence excerpts

### E01 - short_term

`<RECENT_TURNS> user: Ten du an ca nhan cua toi la ORCHID-27. Toi thich Python va khong thich Java. Khi giai thich code, hay dung vi du ngan. assistant: Da hieu: demo ca nhan ORCHID-27, uu tien Python, tranh Java, vi du ngan. user: Toi dang hoc async/await va hay nham coroutine voi Task. Neu sau nay gap chu de nay, hay giai thich bang timeline. assistant: Toi se uu tien timeline khi giai thich coroutine va Task. user: TODO: hoan thanh benchmark report truoc thu Sau luc 16:00. Day la open loop LAB-REPORT-1600. </RECENT_TURNS>`

### E06 - semantic

`EPISODE: For POST /payments, every retryable request MUST send the same Idempotency-Key. Retry only HTTP 429 or transient 5xx errors, use exponential-backoff, and stop after max-3-retries. Marker: PAYMENT-RULE-3. EPISODE: {"id":"kb-payment-retry","entity":"Payment API Retry Policy","summary":"For POST /payments, every retryable request MUST send the same Idempotency-Key. Retry only HTTP 429 or transient 5xx errors, use exponential-backoff, and stop after max-3-retries. Marker: PAYMENT-RULE-3.","source":"internal-api-guideline-v3","updated_at":"2026-08-10T00:00:00Z"} metadata=`

### E09 - long_term

`}: Toi la Lan. Du an cua toi la LOTUS-88. Toi uu tien Java va Spring Boot, va khong dung Python trong vi du backend. The user's project is LOTUS-88. They prioritize Java and Spring Boot for backend development and do not use Python. Content: Lab Assistant (assistant): Da hieu: LOTUS-88, Java + Spring Boot cho backend examples. - LOTUS-88 uses Java + Spring Boot for backend examples. (2026-08-01 11:00:20) Summary: Da hieu uses Java + Spring Boot for backend examples, specifically for LOTUS-88. Summary: The user's project is LOTUS-88. They prioritize Java and Spring Boot for backend development and do not use Python. - Lan Tran is working on the project LOTUS-88. (2026-08-01 11:00:00) - Name: `

### E10 - short_term

`<SESSION_SUMMARY> user: Constraint: REVIEW-DEADLINE-1600 - project review is Friday at 16:00 and must not be forgotten. | assistant: Acknowledged review constraint. | user: Filler turn 1 about UI spacing. | assistant: Filler answer 1. | user: Filler turn 2 about naming. | assistant: Filler answer 2. | user: Filler turn 3 about logging. | assistant: Filler answer 3. </SESSION_SUMMARY> <DURABLE_NOTES> - user: Constraint: REVIEW-DEADLINE-1600 - project review is Friday at 16:00 and must not be forgotten. - assistant: Acknowledged review constraint. </DURABLE_NOTES> <RECENT_TURNS> user: Filler turn 4 about tests. assistant: Filler answer 4. user: Filler turn 5 about docs. assistant: Filler answe`

### E02 - long_term

`- Minh Nguyen uses Python for personal demos on ORCHID-27. (2026-08-05 08:00:00) FACT: Minh Nguyen's personal project is ORCHID-27. [valid_at=2026-08-01T09:00:00Z, invalid_at=None] }: Cuoi tuan minh ngoi mot minh lam demo rieng, khong hop team. Truoc khi chon template, nhac lai: khi lam viec ca nhan minh uu tien ngon ngu nao, va ma du an demo ca nhan la gi? Chi preference cua Minh, dung tron so thich dong nghiep. - Minh Nguyen still prefers Python for personal demos. (2026-08-05 08:00:00) Minh's personal project is named ORCHID-27, for which Minh prefers Python. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS. Minh needs to complete the benchmark report by Fr`

### E03 - long_term

`Summary: Minh Nguyen needs to complete the benchmark report before Friday at 16:00. This is an open-loop report designated as LAB-REPORT-1600. - Minh Nguyen uses Python for personal demos on ORCHID-27. (2026-08-05 08:00:00) - Minh Nguyen's personal project is ORCHID-27. (2026-08-01 09:00:00) }: Minh con mot open-loop phai nop truoc deadline, dong thoi muon ghi chu retry payment dung so lan toi da theo policy. Nac lai ma task/deadline con dang do, va gioi han retry chinh thuc trong lab. Minh's personal project is named ORCHID-27, for which Minh prefers Python. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS. Minh needs to complete the benchmark report by Frida`

### E04 - episodic

`EPISODE: Cach hieu qua la reuse aiohttp ClientSession va dat concurrency=20. Reflection: loi chinh la connection churn, khong phai timeout threshold. Ma su co ASYNC-FIX-20. EPISODE: TODO: hoan thanh benchmark report truoc thu Sau luc 16:00. Day la open loop LAB-REPORT-1600. EPISODE: Hom nay toi debug async HTTP. Toi da thu tang timeout len 60s nhung van fail. EPISODE: Toi nay minh viet tool ca nhan de tai hien su co HTTP roi sua dung playbook. Can ba manh: ngon ngu minh thich khi lam mot minh, ma su co async lan truoc, va buoc playbook truoc khi EPISODE: Chuan bi demo ca nhan: ten/ma project rieng cua Minh la gi, va lan async HTTP truoc minh reuse client nhu the nao (kem ma su co)? Khong can`

### E05 - episodic

`EPISODE: Cach hieu qua la reuse aiohttp ClientSession va dat concurrency=20. Reflection: loi chinh la connection churn, khong phai timeout threshold. Ma su co ASYNC-FIX-20. EPISODE: Hom nay toi debug async HTTP. Toi da thu tang timeout len 60s nhung van fail. EPISODE: Ten du an ca nhan cua toi la ORCHID-27. Toi thich Python va khong thich Java. Khi giai thich code, hay dung vi du ngan. EPISODE: TODO: hoan thanh benchmark report truoc thu Sau luc 16:00. Day la open loop LAB-REPORT-1600. EPISODE: Da ghi nhan trajectory: increase timeout khong hieu qua; ClientSession + concurrency=20 giai quyet connection churn. EPISODE: Minh sap viet script ca nhan de tai hien su co latency, muon code dung ngo`

### E07 - mixed

`<LONG_TERM> FACT: Minh Nguyen's personal project is ORCHID-27. [valid_at=2026-08-01T09:00:00Z, invalid_at=None] FACT: Minh Nguyen uses Python for personal demos on ORCHID-27. [valid_at=2026-08-05T08:00:00Z, invalid_at=None] }: Cuoi tuan minh ngoi mot minh lam demo rieng, khong hop team. Truoc khi chon template, nhac lai: khi lam viec ca nhan minh uu tien ngon ngu nao, va ma du an demo ca nhan la gi? Chi preference cua Minh, dung tron so thich dong nghiep. - When explaining code, Minh Nguyen prefers to use short examples. (2026-08-01 09:00:00) FACT: ORCHID-27 prioritizes Python. [valid_at=2026-08-01T09:00:20Z, invalid_at=2026-08-05T08:00:00Z] FACT: ORCHID-27 avoids Java. [valid_at=2026-08-01T`

### E11 - semantic

`EPISODE: When async HTTP calls time out, inspect connection pooling, downstream saturation and concurrency before increasing timeout. Reuse a long-lived client session where possible. Marker: CONN-POOL-FIRST. EPISODE: {"id":"kb-async-http","entity":"Async HTTP Incident Playbook","summary":"When async HTTP calls time out, inspect connection pooling, downstream saturation and concurrency before increasing timeout. Reuse a long-lived client session where possible. Marker: CONN-POOL-FIRST.","source":"incident-playbook-2026","updated_at":"2026-08-11T00:00:00Z"} metadata=`

### E08 - long_term

`- Python is not to be used for the backend of the company project BLUEBIRD-42. (2026-08-05 08:00:00) - For the company project BLUEBIRD-42, NestJS is required for the backend. (2026-08-05 08:00:00) FACT: For the company project BLUEBIRD-42, TypeScript is required for the backend. [valid_at=2026-08-05T08:00:00Z, invalid_at=None] Summary: For the BLUEBIRD-42 project, the backend must use TypeScript with NestJS, and Python is not permitted for the backend of this project. - Name: BLUEBIRD-42 }: Cong ty yeu cau chinh context window cho agent tren dung backend du an cong ty. Minh can biet stack bat buoc cua BLUEBIRD va ty le budget bon tang nho trong lab de cau hinh cho dung, khong dung so thich `
