# AI Reviewer

Claude Code Skill 기반 인터랙티브 기술 면접 도구.
경력자 대상으로 심화 질문, 꼬리질문, 실무 경험, 상황 대처 질문을 진행하고 종합 평가를 제공합니다.

## 사전 요구사항

- [Claude Code CLI](https://docs.anthropic.com/en/docs/claude-code) 설치 완료
- Claude Code 로그인 완료 (`claude` 명령어 사용 가능 상태)

## 초기 세팅

### 1. 프로젝트 클론

```bash
git clone https://github.com/rlarudgh/ai-reviewer.git
cd ai-reviewer
```

### 2. Claude Code 실행

```bash
claude
```

프로젝트 디렉토리에서 `claude`를 실행하면 `.claude/skills/interview/` 하위의 스킬이 자동으로 인식됩니다.

### 3. 스킬 인식 확인

Claude Code 세션에서 다음을 입력하여 스킬이 정상 인식되는지 확인:

```
/interview
```

트랙 선택 안내 메시지가 출력되면 세팅 완료입니다.

## 사용법

### 면접 시작

**방법 1: 트랙을 직접 지정**

```
/interview frontend       # 프론트엔드 (React, Next.js, TypeScript, Vue, FSD, 알고리즘)
/interview backend        # 백엔드 (Spring Boot, Nest.js, FastAPI)
/interview app            # 모바일 앱 (React Native, Flutter)
/interview web-fullstack  # 프론트엔드 + 백엔드 통합
```

**방법 2: 대화형으로 선택**

```
/interview all
```

트랙 선택 메뉴가 표시됩니다:

```
🎯 면접 트랙을 선택해주세요

| # | 트랙            | 주요 평가 영역                              |
|---|----------------|--------------------------------------------|
| 1 | Frontend       | React, Next.js, TypeScript, Vue, FSD, 알고리즘 |
| 2 | Backend        | Spring Boot, Nest.js, FastAPI, DB, 인프라     |
| 3 | App            | React Native, Flutter, 크로스 플랫폼          |
| 4 | Web Fullstack  | Frontend + Backend 통합 평가                  |

번호나 트랙 이름을 입력해주세요.
```

### 이력서 / 포트폴리오 업로드

트랙 선택 후 이력서나 포트폴리오 파일을 제공하면 맞춤형 질문이 가능합니다:

```
📄 이력서나 포트폴리오가 있으시면 파일 경로를 입력해주세요. (PDF, DOCX, MD 지원)
파일이 없으면 Enter를 눌러 건너뛰실 수 있습니다.
```

**사용 예시:**

```
> /interview all
# 트랙 선택: 1 (Frontend)

# 이력서 경로 입력:
> ~/Desktop/resume.pdf

# 또는 건너뛰기:
> (Enter)
```

이력서를 제공하면:
- 기술 스택과 경력에 맞춘 맞춤형 질문
- 포트폴리오 프로젝트 기반 실무 질문
- 경력 연차에 맞는 난이도 자동 조절

### 면접 진행

1. AI 면접관이 한 번에 하나씩 질문을 합니다
2. 자유롭게 답변을 작성합니다
3. 답변 후 1-2문장의 피드백과 함께 다음 질문이 이어집니다
4. 답변 내용에 따라 꼬리질문과 심화 질문이 자동 생성됩니다

**질문 유형:**

| 유형 | 개수 | 설명 |
|------|------|------|
| 기본기 심화 | 2-3개 | 핵심 개념에 대한 심화 질문 |
| 꼬리질문 | 동적 | 답변 내용 기반 심화 프로브 |
| 실무 경험 | 1-2개 | 실제 프로젝트 경험 질문 |
| 상황 대처 | 1-2개 | 특정 문제 상황 대응 방안 |
| 아키텍처 | 1-2개 | 시스템 설계와 의사결정 |

### 면접 종료 및 평가

면접을 마치고 싶을 때:

```
끝
```

또는: `그만`, `평가해줘`, `마침`, `평가`

종료 시 종합 평가 리포트가 생성되어 대화에 표시되고 `docs/interviews/`에 파일로 저장됩니다.

## 평가 리포트

평가 리포트에는 다음 내용이 포함됩니다:

- **점수 요약** - 4개 항목별 점수와 가중 총점
- **상세 평가** - 항목별 코멘트
- **강점 / 보완점** - Top 3
- **추천 학습 방향** - 실무 중심 제안
- **Q&A 전체 로그** - 모든 질문과 답변, 피드백 기록

### 평가 항목

| 항목 | 가중치 | 설명 |
|------|--------|------|
| 기술 이해도 | 40% | 답변 정확성, 개념 깊이, 트레이드오프 인식 |
| 문제 해결력 | 30% | 접근법, 논리성, 엣지 케이스 고려 |
| 실무 경험 | 15% | 구체적 사례, 의사결정 과정, 실패와 학습 |
| 커뮤니케이션 | 15% | 명확성, 구조화, 용어 사용 |

1-10점 척도로 평가되며, 가중치를 적용한 총점이 산출됩니다.

## 트랙별 면접 범위

### Frontend

React, Next.js, TypeScript, Vue, 아키텍처

- React 렌더링 최적화, hooks 심화, 상태 관리 아키텍처
- Next.js SSR/SSG/ISR, App Router, Server Components
- TypeScript 고급 타입, 제네릭, 런타임 검증 (zod/valibot)
- Vue 2/3 마이그레이션, Composition API, Pinia
- Feature-Sliced Design, Clean Architecture 적용
- 알고리즘: 그래프 탐색, DP, 복잡도 분석

### Backend

Spring Boot, Nest.js, FastAPI

- Spring 트랜잭션, JPA N+1, QueryDSL, 캐시 전략 (Redis)
- Nest.js 모듈/DI, Guard/Interceptor, 마이크로서비스
- FastAPI 비동기, Pydantic, ASGI 배포
- 공통: DB 설계, 인증/인가 (JWT/OAuth2), 장애 대응, 모니터링, CI/CD

### App

React Native, Flutter

- Bridge 모델, New Architecture (Fabric/TurboModules), JSI
- Widget 시스템, 상태 관리 (Riverpod/Bloc), 네이티브 연동
- 앱스토어 배포, CodePush, 푸시 알림, 크로스 플랫폼 트레이드오프

### Web Fullstack

Frontend + Backend 통합 평가

- 프론트엔드와 백엔드 주제를 교차로 진행
- API 설계, 프론트-백 연동, 풀스택 아키텍처 의사결정 포함

## 프로젝트 구조

```
ai-reviewer/
├── .claude/skills/interview/
│   ├── SKILL.md                    # /interview 스킬 진입점 (v2.0)
│   ├── prompts/
│   │   ├── interviewer-system.md   # 면접관 페르소나 & 인터랙션 규칙
│   │   ├── frontend.md             # 프론트엔드 질문 가이드
│   │   ├── app.md                  # 모바일 앱 질문 가이드
│   │   ├── server.md               # 백엔드 질문 가이드
│   │   └── evaluator.md            # 평가 에이전트 프롬프트
│   └── rubric.md                   # 평가 기준표 (1-10점)
├── .claude/skills/interview-tester/ # 프롬프트 QA 자동화
├── .claude/skills/rubric-generator/ # 새 트랙 rubric 생성
├── .claude/skills/interview-analyzer/ # 면접 기록 메타 분석
├── docs/interviews/                # 면접 결과 저장소 (gitignore)
├── CLAUDE.md                       # 프로젝트 설정
└── README.md
```

## 추가 스킬

| 명령어 | 설명 |
|--------|------|
| `/interview-tester {track}` | 프롬프트 QA 자동화 (가상 후보자로 면접 테스트) |
| `/rubric-generator {track}` | 새 트랙 rubric/질문 가이드 자동 생성 |
| `/interview-analyzer` | 면접 기록 메타 분석 리포트 |
