# AI Reviewer

Claude Code 기반 기술 면접 도구.

## Skills

### 면접 진행
- `/interview frontend` - React, Next.js, TypeScript, Vue, 아키텍처(FSD), 알고리즘 면접
- `/interview app` - React Native, Flutter 면접
- `/interview server` - Spring Boot, Nest.js, FastAPI 면접
- `/interview` - 트랙 선택 안내

### 품질 관리
- `/interview-tester {track}` - 프롬프트 QA 자동화 (가상 후보자로 면접 테스트)
- `/rubric-generator {track}` - 새 트랙 rubric/질문 가이드 자동 생성
- `/interview-analyzer` - 면접 기록 메타 분석 리포트

## 면접 종료

면접 마지막 질문 완료 후 자동 평가 리포트 생성 및 `docs/interviews/`에 저장.
"끝", "평가해줘", "그만" 등 입력 시에도 즉시 평가 가능.

## Project Structure

```
.claude/skills/
├── interview/
│   ├── SKILL.md                    # 면접 스킬 진입점
│   ├── prompts/
│   │   ├── interviewer-system.md   # 면접관 페르소나
│   │   ├── frontend.md             # 프론트엔드 질문 가이드
│   │   ├── app.md                  # 앱 질문 가이드
│   │   ├── server.md               # 서버 질문 가이드
│   │   └── evaluator.md            # 평가 에이전트
│   └── rubric.md                   # 평가 기준표
├── interview-tester/               # 프롬프트 QA 자동화
├── rubric-generator/               # 새 트랙 rubric 생성
└── interview-analyzer/             # 면접 기록 메타 분석

docs/
├── interviews/                     # 면접 결과 저장소 (gitignore)
├── examples/                       # 골든셋 평가 리포트 샘플
├── PRD.md                          # 제품 요구사항
├── ROADMAP.md                      # 프로젝트 로드맵
├── PROMPT_ENGINEERING.md           # 프롬프트 설계 가이드
└── SKILL_DEVELOPMENT_GUIDE.md      # 스킬 개발 가이드

tests/                              # 테스트 구조
assets/                             # 참고 자료
```
