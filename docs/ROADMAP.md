# AI Reviewer Roadmap

Claude Code 기반 기술 면접 도구의 발전 방향.

---

## v1.0 — MVP

- [x] 프론트엔드 트랙 (React, Next.js, TypeScript)
- [x] 앱 트랙 (React Native, Flutter)
- [x] 서버 트랙 (Spring Boot, Nest.js, FastAPI)
- [x] 인터랙티브 면접 진행 (8-12 질문)
- [x] 자동 평가 리포트 생성
- [x] 평가 결과 파일 저장 (`docs/interviews/`)
- [x] 평가 기준표 (rubric) 기반 점수 산정

---

## v2.0 — 현재 (UX 고도화)

- [x] `/interview all` 대화형 트랙 선택 메뉴
- [x] Web Fullstack 트랙 (Frontend + Backend 통합)
- [x] Backend 트랙 별칭 (`server` → `backend`)
- [x] 이력서/포트폴리오 업로드 (PDF, DOCX, MD)
- [x] 이력서 기반 맞춤형 질문 생성
- [x] Q&A 전체 로그 추적 및 리포트 포함
- [x] 평가 리포트에 후보자명, 일시 정보 추가
- [x] **interview-tester**: 프롬프트 QA 자동화
- [x] **rubric-generator**: 새 트랙 rubric 자동 생성
- [x] **interview-analyzer**: 면접 기록 메타 분석
- [x] 골든셋 평가 리포트 샘플

---

## v2.1 — 품질 관리 (Short-term)

- [ ] 프롬프트 단위 테스트 환경 구축
- [ ] 이력서 분석 정확도 개선

---

## v2.2 — 트랙 확장 (Mid-term)

- [ ] **DevOps 트랙** (Docker, Kubernetes, CI/CD, AWS/GCP)
- [ ] **AI/ML 트랙** (PyTorch, TensorFlow, MLOps, LLM)
- [ ] **Database 트랙** (PostgreSQL, Redis, MongoDB, 설계 패턴)
- [ ] **System Design 트랙** (분산 시스템, MSA, 확장성)
- [ ] 커스텀 트랙 생성 가이드 제공

---

## v3.0 — 고도화 (Long-term)

- [ ] **난이도 분리**: Junior / Mid / Senior 레벨별 질문 난이도 조절
- [ ] **다국어 지원**: 영어, 일본어 면접 진행
- [ ] **기업별 맞춤 트랙**: 특정 기업의 기술 스택에 맞춘 면접 커스터마이징
- [ ] **협동 면접**: 다수의 면접관이 동시에 평가하는 워크플로우
- [ ] **리포트 내보내기**: Markdown → PDF, Notion 변환
- [ ] **면접 히스토리 대시보드**: 시간별 점수 추이, 약점 개선 추적

---

## 기여 아이디어

새로운 아이디어나 제안은 [Issues](../../issues)에 등록해주세요.

- 새 트랙 제안 → `/rubric-generator` 로 초안 생성 → 리뷰 후 병합
- 프롬프트 개선 → `/interview-tester` 로 QA → 결과 비교 후 병합
- 번역 기여 → `prompts/` 디렉토리 내 다국어 프롬프트 추가
