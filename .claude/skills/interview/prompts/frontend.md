# Frontend Track - React, Next.js, TypeScript

프론트엔드 엔지니어링 실무 역량을 평가합니다. 경력자 대상으로 기본 개념이 아닌 심화 주제와 실무 적용에 집중합니다.

## Topic Guide

### React 심화
- 렌더링 최적화: reconciliation 알고리즘, memo/callback 전략, 렌더링 성능 프로파일링
- Hooks 아키텍처: custom hooks 설계 패턴, hooks 규칙의 내부 동작, useRef/useMemo/useCallback 사용 기준
- 상태 관리: Context API의 한계, Redux Toolkit vs Zustand vs Jotai 선택 기준, 서버 상태(TanStack Query)와 클라이언트 상태 분리
- 동시성: React 18 Concurrent Features, Suspense, Transition, useDeferredValue 실무 적용
- 에러 처리: Error Boundary, 선언적 에러 처리, 비동기 에러 캐치 전략

### Next.js
- 렌더링 전략: SSR vs SSG vs ISR 선택 기준, App Router의 Server Components 활용
- 라우팅: App Router와 Pages Router 차이, Middleware, Dynamic Routes, Parallel Routes
- 최적화: Image/Font/Script 최적화, Bundle 분석, Code Splitting 전략
- 데이터 페칭: Server Actions, RSC 패턴, 캐싱과 revalidation 전략
- 배포: Vercel vs 자체 호스팅, Edge Runtime vs Node.js Runtime

### TypeScript
- 고급 타입: Conditional Types, Mapped Types, Template Literal Types 활용
- 제네릭: 제네릭 설계, constrained generics, 타입 추론 활용
- 타입 안전성: 타입 가드, discriminated unions, exhaustive checking
- 실무 패턴: API 응답 타입 설계, Form 타입 안전성, 런타임 검증(zod/valibot)과 정적 타입 연동

### 아키텍처 & 설계
- Feature-Sliced Design: 레이어 구조(app → pages → widgets → features → entities → shared), 슬라이스 분리 기준, 의존성 규칙
- Clean Architecture: 프레젠테이션/도메인/데이터 계층 분리, 의존성 역전 원칙, 프론트엔드에서의 적용 한계와 트레이드오프
- 컴포넌트 설계: Atomic Design vs 컴파운드 컴포넌트 패턴, Headless UI 아키텍처, 제어/비제어 컴포넌트 전략
- 모듈 경계: barrel export, public API 명세, 순환 의존성 탐지와 해결
- 실무 비교: FSD vs 도메인 기반 폴더 구조 vs 기능 기반 구조, 프로젝트 규모에 따른 선택 기준

### 알고리즘 & CS 기초
- 그래프 탐색: DFS/BFS 원리, 시간/공간 복잡도, 프론트엔드 응용(DOM 트리 순회, 의존성 그래프, 라우팅)
- 동적 계획법: DP 접근법(top-down/memoization vs bottom-up/tabulation), 최적 부분 구조와 중복 부분 문제 식별
- 자료구조: 트리(컴포넌트 트리, AST), 해시 테이블(가상 DOM diffing), 큐/스택(이벤트 루프, 호출 스택)
- 복잡도 분석: Big-O 표기법, 렌더링 알고리즘 복잡도 분석, n개 리스트 렌더링 시 성능 예측
- 실무 연계: 가상 DOM reconciliation의 알고리즘적 접근, 번들러의 의존성 그래프 순회, 무한 스크롤 데이터 관리 전략

### Vue.js (실무 경험 기반)
- Vue 2 아키텍처: Options API, 반응형 시스템(Object.defineProperty 기반), computed/watch 동작 원리
- Vue 2 → Vue 3 마이그레이션: Composition API 도입, Proxy 기반 반응형 전환, breaking changes 대응 전략
- 상태 관리: Vuex 모듈 구조화, namespaced modules, Vue 3에서의 Pinia 전환
- 성능 최적화: Vue 2 한계(React.memo 불가 → v-once, 함수형 컴포넌트 활용), 가상 스크롤, 지연 렌더링
- 실무 경험: 대규모 폼, 무한 스크롤, 컴포넌트 통신 패턴(event bus vs Vuex vs provide/inject)

### 실무 시나리오 예시
- "대규모 폼(50+ 필드)에서 성능 저하가 발생합니다. 어떻게 최적화하시겠어요?"
- "페이지 로드 시 LCP가 4초 이상입니다. 진단과 개선 프로세스를 설명해주세요."
- "MSW 기반 테스트 환경에서 실제 API와 스펙이 달라 문제가 발생했습니다. 어떻게 방지하시겠어요?"
- "디자인 시스템 컴포넌트 라이브러리를 만들어야 합니다. 아키텍처를 어떻게 설계하시겠어요?"
- "FSD 아키텍처에서 features 레이어 간 의존성이 생기면 어떻게 해결하시겠어요?"
- "Vue 2 프로젝트에서 수백 개 아이템의 무한 스크롤 성능을 최적화해야 합니다. 어떻게 접근하시겠어요?"
- "DOM 트리에서 특정 조건의 노드를 찾아야 합니다. DFS와 BFS 중 어떤 방식을 선택하시겠고 이유는?"

### 경력 질문 예시
- "프론트엔드 상태 관리 라이브러리를 교체한 경험이 있나요? 마이그레이션 전략은?"
- "Next.js 마이그레이션을 진행한 적이 있다면, 가장 어려웠던 부분은?"
- "퍼포먼스 모니터링을 도입한 경험이 있나요? 어떤 메트릭을 추적했나요?"
- "프론트엔드 CI/CD 파이프라인을 구축한 경험이 있다면 핵심 구성을 설명해주세요."
- "FSD나 다른 아키텍처 패턴을 실제 프로젝트에 도입해본 경험이 있나요? 도입 과정과 효과는?"
- "Vue 2에서 React로 전환한 경험이 있다면, 두 프레임워크의 차이에서 오른 가장 큰 어려움은?"
- "알고리즘이나 자료구조 지식이 실무 문제 해결에 도움이 된 경험이 있나요?"
