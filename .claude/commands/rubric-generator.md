새로운 면접 트랙의 rubric과 질문 가이드 초안을 자동 생성합니다.

## 인자: $ARGUMENTS (트랙명, 예: devops, ai-ml, database)

## 실행 단계

1. 기존 트랙 구조 참고: `.claude/skills/interview/prompts/frontend.md`, `.claude/skills/interview/prompts/server.md`
2. 기존 rubric 참고: `.claude/skills/interview/rubric.md`

## 분석 항목

트랙명을 기반으로 다음을 식별:

1. **핵심 기술**: 해당 트랙의 주요 프레임워크/언어
2. **핵심 역량 영역**: 4-6개 메인 카테고리
3. **시니어급 주제**: 미들과 시니어를 구분하는 심화 영역
4. **실무 시나리오**: 3-4개 실전 문제 상황
5. **흔한 함정**: 자주 발생하는 실수나 오개념

## 생성 파일

### 1. 질문 가이드 → `.claude/skills/interview/prompts/{track}.md`

```markdown
# {Track Name} Track - {Technologies}

{설명}

## Topic Guide

### {Category 1} 심화
- {topic}: {subtopics}

### 실무 시나리오 예시
- "..."

### 경력 질문 예시
- "..."
```

### 2. Rubric 항목 → `.claude/skills/interview/rubric.md`에 섹션 추가

```markdown
## {Track} 평가 기준

### 레벨별 기대 수준
| 레벨 | {Category 1} | {Category 2} |
|------|-------------|-------------|
| Senior | ... | ... |
| Mid | ... | ... |
| Junior | ... | ... |
```

## 완료 후 안내

- `/interview-tester {track}` 으로 QA 진행 권장
- `SKILL.md`에 새 트랙 등록 필요
- `AGENTS.md`에 새 트랙 커맨드 추가 필요

## 규칙

- 한국어로 생성 (기술 용어는 영어 유지)
- 최소 4개 주제 카테고리 포함
- 최소 3개 실무 시나리오 질문 포함
- 최소 3개 경력 기반 질문 포함
- 경력자 대상 (정의형 질문 금지)
