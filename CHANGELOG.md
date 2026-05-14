# Changelog

모든 주요 변경 사항은 이 문서에 기록됩니다.

형식은 [Keep a Changelog](https://keepachangelog.com/ko/1.1.0/)를 따륩니다.

## [1.0.0] - 2026-05-13

### Added
- Claude Code Skill 기반 인터랙티브 기술 면접 시스템 출시
- 3가지 면접 트랙 지원:
  - **Frontend**: React, Next.js, TypeScript, Vue, 아키텍처(FSD), 알고리즘
  - **App**: React Native, Flutter
  - **Server**: Spring Boot, Nest.js, FastAPI
- 3단계 면접 워크플로우 (Setup → Interview → Evaluation)
- 동적 꼬리질문 및 실시간 난이도 조절
- 4가지 평가 항목 기반 종합 평가 리포트 (기술 이해도, 문제 해결력, 실무 경험, 커뮤니케이션)
- 1-10점 세부 평가 기준표 (rubric)
- 면접관 페르소나 및 상호작용 규칙 프롬프트
- 한국어 면접 진행, 기술 용어 영어 유지
- 스킬 개발 가이드 문서 작성
- GitHub Actions 기본 CI 구성
- 면접 종료 시 자동 평가 리포트 생성 및 `docs/interviews/`에 파일 저장
- 프롬프트 QA 자동화 명령어 (`/interview-tester`)
- 새 트랙 rubric/질문 가이드 자동 생성 명령어 (`/rubric-generator`)
- 면접 기록 메타 분석 명령어 (`/interview-analyzer`)
- 골든셋 평가 리포트 샘플 (`docs/examples/frontend_golden_set.md`)

### Technical
- `.claude/` 구조 분리 설계:
  - `skills/` — 대화형 면접 (multi-phase, interactive)
  - `commands/` — 단발성 유틸 (QA, 생성, 분석)
  - `rules/` — 항상 로드되는 공통 규칙
  - `settings.json` — 권한 설정
- 5개 프롬프트 파일 분리 (interviewer-system, frontend, app, server, evaluator)
- `rubric.md` 평가 기준 분리
- `AGENTS.md` 및 `CLAUDE.md` 프로젝트 규칙 정의
- PR 템플릿에 프롬프트 품질 체크리스트 추가
- `docs/interviews/` gitignore 처리 (면접 결과 파일은 Git에 올라가지 않음)

## [Unreleased]

### Planned
- 새로운 기술 면접 트랙 추가 (DevOps, AI/ML, 데이터 엔지니어링 등)
- 커스텀 평가 기준 설정
- **경력 수준별 면접 레벨** (신입/주니어/시니어) — `SKILL.md`, `rubric.md`, 프롬프트 분기 필요
- 다중 언어 지원 (영어, 일본어)
- 면접 질문 품질 개선 및 확장

## [2.0.0] - 2026-05-14

### Added
- **`/interview all` 대화형 트랙 선택** — 번호 또는 이름으로 트랙을 선택하는 메뉴 UI
- **Web Fullstack 트랙** — Frontend + Backend 주제를 교차로 진행하는 통합 면접
- **이력서/포트폴리오 업로드** — PDF, DOCX, MD 파일 경로를 입력하면 분석 후 맞춤형 질문 생성
- **Q&A 전체 로그** — 면접 중 모든 질문-답변-피드백을 추적하여 평가 리포트에 포함
- **Backend 트랙 별칭** — 기존 `server` 트랙을 `backend`로도 접근 가능

### Changed
- `SKILL.md` v1.0 → v2.0 (Phase 1에 트랙 선택 및 이력서 업로드 단계 추가)
- `evaluator.md` 평가 리포트 템플릿에 후보자명, 일시, Q&A 로그 섹션 추가
- `interviewer-system.md`에 이력서 기반 맞춤 질문 가이드 추가
- `AGENTS.md` 스킬 목록에 `backend`, `web-fullstack`, `all` 반영
- `README.md` v2.0 사용법 전면 업데이트

### Removed
- ~~`/interview server`~~ → `/interview backend`로 통합 (기존 `server` 명령어도 호환)
