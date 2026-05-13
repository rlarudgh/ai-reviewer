# Server Track - Spring Boot, Nest.js, FastAPI

백엔드 엔지니어링 실무 역량을 평가합니다. 아키텍처 설계, 데이터베이스, 장애 대응, 확장성에 집중합니다.

## Topic Guide

### Spring Boot
- 핵심: Bean 라이프사이클, ApplicationContext, @Transactional 전파 속성과 격리 수준
- JPA/Hibernate: N+1 문제 해결, 지연 로딩 전략, QueryDSL/Fetch Join 활용, 엔티티 설계
- 성능: 커넥션 풀 튜닝, 캐시 전략(Redis), 배치 처리 최적화
- 테스트: @DataJpaTest 슬라이스 테스트, TestContainers, 통합 테스트 전략
- 보안: Spring Security 필터 체인, JWT/OAuth2 인증, CORS, CSRF

### Nest.js
- 아키텍처: 모듈 시스템, DI 컨테이너, Guard/Interceptor/Pipe 필터 체인
- 데이터베이스: TypeORM/Prisma 선택, 트랜잭션 관리, 마이그레이션 전략
- 실시간: WebSocket Gateway, Socket.IO, 이벤트 기반 아키텍처
- 마이크로서비스: Message Pattern, Transport 계층, gRPC 연동
- 테스팅: Jest 단위 테스트, E2E 테스트, 모듈 mocking

### FastAPI
- 비동기: async/await 패턴, 이벤트 루프, 비동기 DB 드라이버(asyncpg/aiomysql)
- 검증: Pydantic 모델 설계, 커스텀 validator, 중첩 스키마
- 아키텍처: Dependency Injection, 미들웨어, 라우터 구조화
- 배포: Uvicorn/Gunicorn 워커, Docker 최적화, ASGI 서버 선택
- 테스팅: pytest-asyncio, TestClient, 픽스처 설계

### 공통 백엔드 주제
- 데이터베이스: 인덱스 설계, 쿼리 최적화, 정규화/반정규화 기준, 분산 DB
- API 설계: RESTful 원칙, GraphQL 도입 기준, API 버전 관리, 에러 응답 표준화
- 캐시: 캐시 전략(Cache-Aside/Write-Through), 캐시 무효화, TTL 설계
- 인증/인가: JWT 세부 설계, Refresh Token 로테이션, RBAC/ABAC
- 장애 대응: Circuit Breaker, Rate Limiting, Graceful Degradation, 장애 전파 방지
- 모니터링: 로깅 전략, 분산 추적(Tracing), 메트릭 수집, 알림 설계
- 인프라: Docker 컨테이너화, CI/CD 파이프라인, 블루그린/카나리 배포

### 실무 시나리오 예시
- "프로덕션 DB에서 Deadlock이 빈번하게 발생합니다. 원인 분석과 해결 방안은?"
- "트래픽이 10배 증가했습니다. 수평 확장 전략과 병목 지점은?"
- "SQL Injection 공격이 감지되었습니다. 즉각 대응과 장기적 예방 조치를 각각 설명해주세요."
- "MSA 환경에서 서비스 간 트랜잭션 일관성을 어떻게 보장하시겠어요?"
- "배치 작업이 점점 느려지고 있습니다. 원인 진단과 개선 방안은?"

### 경력 질문 예시
- "레거시 모놀리식을 MSA로 전환한 경험이 있나요? 가장 어려웠던 점은?"
- "프로덕션 장애 대응 중 가장 기억에 남는 사례를 설명해주세요."
- "DB 마이그레이션을 진행한 경험이 있나요? 무중단 마이그레이션 전략은?"
- "백엔드 성능 튜닝에서 가장 큰 효과를 봤던 경험을 설명해주세요."
- "팀 코드 리뷰 문화를 개선한 경험이 있나요?"
