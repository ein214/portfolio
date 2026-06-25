# Portfolio

🌐 **[라이브 사이트](https://ein214.github.io/portfolio/)** · 👤 **[전체 프로필](https://github.com/ein214)**

백엔드 작업 기록을 도메인별로 정리했습니다.

---

## 정산 시스템

수기 엑셀 정산을 시스템으로 옮긴 0→1 설계(1)와 데이터가 천만 건대로 쌓인 뒤 드러난 조회 성능 문제(2)를 다룹니다.

| # | 글 | 한 줄 요약 | 키워드 |
|---|---|---|---|
| 1 | **[정산 플랫폼 0→1 설계](./troubleshooting/settlement-system-zero-to-one.md)** | 수기 엑셀 정산을 시스템으로. 1:N 저작권 분배와 이용권 일할 정산이 핵심 난제 | 도메인 모델링 · 1:N 수익 분배 · 운영 자립화 |
| 2 | **[천만 건 조회 개선](./troubleshooting/settlement-query-optimization.md)** | 인덱스도 파티셔닝도 통하지 않은 이유. 읽기 모델을 분리(CQRS) | PostgreSQL 실행계획 · 파티셔닝 효과 범위 · CQRS · 비정규화 |

> 설계 배경과 아키텍처 다이어그램은 **[정산 시스템 Deep Dive](https://ein214.github.io/portfolio/settlement.html)** 에 정리돼 있습니다.

---

## 백그라운드 큐·워커 (Bull · Redis)

파일 다운로드 워터마크를 처리하는 백그라운드 워커에서 겪은 두 건의 장애 기록입니다.

| # | 글 | 한 줄 요약 | 키워드 |
|---|---|---|---|
| 3 | **[Bull Queue 워터마크 병목](./troubleshooting/bull-queue-bottleneck.md)** | 개별 작업은 1~5초인데 대기는 31분. 처리 속도가 아니라 처리 용량이 원인 | concurrency 설계 · 멱등성 · Graceful Shutdown · 경량 분산 락 |
| 4 | **[RSS 메모리 누수 추적](./troubleshooting/redis-job-memory-leak.md)** | heap은 정상인데 RSS만 우상향. 네이티브 라이브러리가 메모리를 반환하지 않은 문제 | 네이티브 메모리 · V8 GC와 RSS · glibc malloc arena |

---

## 백오피스 공통화

| 글 | 한 줄 요약 | 키워드 |
|---|---|---|
| **[ListBuilder — AdminJS 리스트 페이지 빌더](https://ein214.github.io/portfolio/listbuilder/)** | 리스트 페이지마다 반복되던 조회·필터·정렬·엑셀 로직을 설정 객체로 선언하는 재사용 빌더로 공통화. 관리자 페이지 10여 곳에 적용 | 선언형 config · 로직/표현 분리 · 확장 포인트 |

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
