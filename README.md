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

```bash
/interview
```

트랙 선택 안내 메시지가 출력되면 세팅 완료입니다.

## 사용법

### 면접 시작

원하는 트랙을 지정하여 면접을 시작합니다:

```bash
/interview frontend   # 프론트엔드 면접 (React, Next.js, TypeScript)
/interview app        # 모바일 앱 면접 (React Native, Flutter)
/interview server     # 백엔드 면접 (Spring Boot, Nest.js, FastAPI)
```

### 면접 진행

1. AI 면접관이 한 번에 하나씩 질문을 합니다
2. 자유롭게 답변을 작성합니다
3. 답변 후 1-2문장의 피드백과 함께 다음 질문이 이어집니다
4. 답변 내용에 따라 꼬리질문과 심화 질문이 자동 생성됩니다

질문 유형:

- **기본기 질문** - 핵심 개념에 대한 심화 질문 (2-3개)
- **꼬리질문** - 답변 내용을 바탕으로 한 심화 프로브
- **실무 경험 질문** - 실제 프로젝트 경험에 대한 질문 (1-2개)
- **상황 대처 질문** - 특정 문제 상황에 대한 대응 방안 (1-2개)
- **아키텍처 질문** - 시스템 설계와 의사결정 (1-2개)

### 면접 종료 및 평가

면접을 마치고 싶을 때:

```bash
끝
```

또는 다음과 같이 입력해도 됩니다: `그만`, `평가해줘`, `마침`, `평가`

종료 시 대화 전체 기록을 분석하여 종합 평가 리포트가 생성됩니다.

## 평가 항목

| 항목         | 가중치 | 설명                                      |
| ------------ | ------ | ----------------------------------------- |
| 기술 이해도  | 40%    | 답변 정확성, 개념 깊이, 트레이드오프 인식 |
| 문제 해결력  | 30%    | 접근법, 논리성, 엣지 케이스 고려          |
| 실무 경험    | 15%    | 구체적 사례, 의사결정 과정, 실패와 학습   |
| 커뮤니케이션 | 15%    | 명확성, 구조화, 용어 사용                 |

평가는 1-10점 척도로 진행되며, 가중치를 적용한 총점이 산출됩니다.

## 트랙별 면접 범위

### Frontend (React, Next.js, TypeScript)

- React 렌더링 최적화, hooks 심화, 상태 관리 아키텍처
- Next.js SSR/SSG/ISR, App Router, 캐싱 전략
- TypeScript 고급 타입, 제네릭, 런타임 검증

### App (React Native, Flutter)

- Bridge 아키텍처, New Architecture, 성능 최적화
- Widget 시스템, 상태 관리, 네이티브 연동
- 앱스토어 배포, OTA 업데이트, 크로스 플랫폼 트레이드오프

### Server (Spring Boot, Nest.js, FastAPI)

- Spring 트랜잭션, JPA N+1, 캐시 전략
- Nest.js 모듈/가드, 마이크로서비스
- FastAPI 비동기, Pydantic, ASGI 배포
- 공통: DB 설계, 인증/인가, 장애 대응, 모니터링

## 프로젝트 구조

```
ai-reviewer/
├── .claude/skills/interview/
│   ├── SKILL.md                    # /interview 스킬 진입점
│   ├── prompts/
│   │   ├── interviewer-system.md   # 면접관 페르소나 & 인터랙션 규칙
│   │   ├── frontend.md             # 프론트엔드 트랙 질문 가이드
│   │   ├── app.md                  # 모바일 앱 트랙 질문 가이드
│   │   ├── server.md               # 백엔드 트랙 질문 가이드
│   │   └── evaluator.md            # 평가 에이전트 프롬프트
│   └── rubric.md                   # 평가 기준표 (1-10점)
├── CLAUDE.md                       # 프로젝트 설정
└── README.md
```
