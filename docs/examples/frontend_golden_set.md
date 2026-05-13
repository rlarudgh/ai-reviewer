# Example: Frontend Interview Evaluation Report (Golden Set)

골든셋 — 프롬프트 품질 비교의 기준이 되는 평가 리포트 샘플.

---

## 기술 면접 총평

**트랙:** Frontend (React, Next.js, TypeScript)
**진행 질문 수:** 10개

---

### 점수 요약

| 평가 항목 | 점수 (1-10) | 가중치 | 가중 점수 |
|-----------|-------------|--------|----------|
| 기술 이해도 | 7.5 | 40% | 3.00 |
| 문제 해결력 | 7.0 | 30% | 2.10 |
| 실무 경험 | 8.0 | 15% | 1.20 |
| 커뮤니케이션 | 7.5 | 15% | 1.13 |
| **총점** | | | **7.4/10** |

---

### 상세 평가

#### 기술 이해도 (7.5/10)
- React Concurrent Features에 대한 이해도 높음. `useTransition`의 non-urgent update 개념을 정확히 설명하고, Suspense와의 연동까지 언급
- Next.js App Router에서 Server/Client Components의 경계를 실무 기준(interactivity 유무)으로 명확히 구분
- TypeScript 제네릭 설계에서 constrained generics의 필요성을 실제 API 응답 타이핑 사례로 설명
- Web Streams API나 RSC의 직렬화 제약 같은 심화 주제에서는 깊이가 약간 부족

#### 문제 해결력 (7.0/10)
- LCP 4초 문제 진단 시 Lighthouse → DevTools Performance 탭 → 번들 분석 도구로 이어지는 체계적 접근
- 대규모 폼 최적화에서 React Hook Form + zod 조합의 이유를 명확히 설명 (리렌더링 최소화 + 런타임 검증)
- "모든 케이스를 커버하는 솔루션은 없다"며 트레이드오프를 인정하는 태도 좋음
- 엣지 케이스(네트워크 단절 시 동작)에 대한 고려는 아쉬움

#### 실무 경험 (8.0/10)
- 마이크로 프론트엔드 도입 경험을 Module Federation의 한계와 webpack 대안 선택 이유까지 구체적으로 설명
- TanStack Query 마이그레이션 시 서버 상태와 클라이언트 상태를 분리한 전략이 실무적
- 디자인 시스템에서 compound component 패턴과 cva를 활용한 variant 관리까지 언급
- 프로덕션 장애 대응 경험(Sentry → 롤백 → 포스트모템)이 구체적

#### 커뮤니케이션 (7.5/10)
- 서론-본론-결론 구조로 답변하여 전달력이 좋음
- 기술 용어를 정확하게 사용하고, 필요시 비기술자에게 설명하듯 비유 활용
- 질문의 의도를 정확히 파악하여 핵심에 집중
- 복합 질문에서 후반부를 놓치는 경우 가끔 있음

---

### 강점 (Top 3)
1. **실무 기반 의사결정**: 기술 선택 시 트레이드오프를 명확히 인지하고, 팀/프로젝트 맥락에서 결정
2. **심화 개념 이해**: React 내부 동작(reconciliation, lane priority)과 Next.js 아키텍처까지 깊이 이해
3. **명확한 커뮤니케이션**: 구조화된 답변과 정확한 기술 용어 사용

### 보완점 (Top 3)
1. **엣지 케이스 고려**: 정상 흐름은 잘 설명하나, 에러/예외 상황에 대한 사고 확장 필요
2. **Web API 심화**: Streams API, Service Worker, Web Workers 등 브라우저 API에 대한 깊이 보완
3. **성능 측정 경험**: Core Web Vitals 개선 사이클을 직접 주도한 경험 추가 필요

### 추천 학습 방향
- **Web Performance 심화**: Chrome DevTools Protocol 활용, RUM(Real User Monitoring) 도입 경험
- **React 소스코드 리딩**: React 내부 reconciler 동작 원리를 코드 레벨에서 이해
- **시스템 설계 연습**: 대규모 프론트엔드 아키텍처 설계 (마이크로 프론트엔드, Module Federation 한계 극복)

---

### 총평 한줄평
실무 경험이 풍부하고 기술적 깊이가 좋은 시니어급 프론트엔드 엔지니어. 엣지 케이스와 브라우저 API 심화만 보완하면 완성도 높은 아키텍트급.
