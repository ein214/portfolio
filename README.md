# Portfolio

🌐 **[라이브 사이트](https://ein214.github.io/portfolio/)** · 🧩 **[정산 시스템 Deep Dive](https://ein214.github.io/portfolio/settlement.html)** · 👤 **[전체 프로필](https://github.com/ein214)**

---

## 읽는 순서

정산 시스템을 0부터 세운 **설계 기록(1)** 에서 출발해, 그 시스템이 천만 건 규모로 성장하며 부딪힌 **문제 해결(2~4)** 로 이어집니다.

| # | 글 | 한 줄 요약 | 키워드 |
|---|---|---|---|
| 1 | **[정산 플랫폼 0→1 설계](./troubleshooting/settlement-system-zero-to-one.md)** | 100% 수동 엑셀 정산을 시스템으로. 1:N 저작권 분배·일할 정산이 핵심 난제 | 도메인 모델링 · 1:N 정산 알고리즘 · 운영 자립화 |
| 2 | **[천만 건 조회 개선](./troubleshooting/settlement-query-optimization.md)** | 인덱스도 파티셔닝도 안 듣던 이유. 결국 읽기 모델을 분리(CQRS) | PostgreSQL 실행계획 · 파티셔닝 효과 범위 · CQRS·비정규화 |
| 3 | **[Bull Queue 워터마크 장애](./troubleshooting/bull-queue-bottleneck.md)** | 처리 능력은 멀쩡한데 31분 대기. "느린 작업"과 "밀린 큐"는 다르다 | 멱등성 설계 · Graceful Shutdown · 멀티 인스턴스 분산 락 |
| 4 | **[RSS 메모리 누수 4일 추적](./troubleshooting/redis-job-memory-leak.md)** | heap은 정상인데 RSS만 우상향. 네이티브 라이브러리의 메모리 미반납 | Native Memory 추적 · V8 GC와 RSS · glibc malloc arena |

> 1번 글의 설계 배경·아키텍처 다이어그램은 **[정산 시스템 Deep Dive](https://ein214.github.io/portfolio/settlement.html)** 에 더 자세히 정리돼 있습니다.

---

<details>
<summary><b>경력 요약 · 기술 스택</b> (펼치기)</summary>

<br>

**(주)북아이피스** · Backend Developer · 2022.05 ~ 재직 중
정산 시스템 0→1 설계·구축(SQS 기반 비동기 정산·1:N 저작권 분배·일할 정산), 정산 조회 전용 Read DB(CQRS) 구축, 저자 라이선스·정산 시스템 개편, Redis Job 메모리 누수 안정화, Watermark Queue 처리량·모니터링 개선, Express→NestJS 점진적 전환, AdminJS 기반 운영 도구 공통화.

**(주)유니윌 / 위즈페이** · 2020.07 ~ 2022.04 · 온라인 교육 플랫폼·정산 시스템 개발, AWS 운영.
**주식회사 큐브시스템** · 2018.04 ~ 2020.06 · 블록체인 월렛·API, Laravel 배치·정산.
**(주)이비즈네트웍스** · 2013.03 ~ 2017.11 · 여행 플랫폼·관리자, 제휴 REST API, 검색 성능 개선.

*초기 경력(2011~2012) 포함 총 14년 2개월. 상세 경력은 [전체 프로필](https://github.com/ein214/ein214) 참고.*

**기술 스택** — Node.js · NestJS · TypeScript · PHP · Laravel / PostgreSQL · MySQL · Redis / AWS(Beanstalk · SQS · S3 · CloudWatch)

</details>
