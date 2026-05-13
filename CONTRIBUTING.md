# Contributing to AI Reviewer

AI Reviewer에 기여해주셔서 감사합니다.

---

## 새로운 트랙 추가하기

면접 트랙은 다음 구조로 구성되어 있습니다:

```sh
.claude/skills/interview/prompts/
├── interviewer-system.md   # 공통 면접관 페르소나 (수정 불필요)
├── frontend.md             # 트랙별 질문 가이드
├── app.md
├── server.md
└── evaluator.md            # 공통 평가 에이전트 (수정 불필요)
```

### 트랙 추가 프로세스

1. **Issue 생성**: `[Track] {트랙명} 트랙 추가 제안` 제목으로 이슈 생성
2. **rubric 생성**: `/rubric-generator {기술명}` 로 rubric과 질문 가이드 초안 자동 생성
3. **프롬프트 작성**: 기존 트랙(`frontend.md`, `server.md`) 구조를 참고하여 보완
4. **QA 진행**: `/interview-tester {트랙명}` 으로 프롬프트 품질 검증
5. **PR 제출**: 변경사항과 QA 결과를 함께 제출

### 프롬프트 작성 가이드라인

- **Topic Guide**: 기술별 심화 주제를 카테고리로 정리
- **실무 시나리오 예시**: 3-4개의 구체적인 상황 질문 포함
- **경력 질문 예시**: 3-4개의 실무 경험 질문 포함
- 경력자 대상이므로 정의형 질문("X란?") 지양, 이유와 트레이드오프에 집중

---

## 프롬프트 수정하기

기존 프롬프트를 개선하는 경우:

1. `EXAMPLES/`의 골든셋과 비교하여 품질 저하가 없는지 확인
2. `/interview-tester` 로 변경 전후 비교
3. PR에 **before/after 비교**를 포함

---

## PR 규칙

- [ ] 관련 Issue 연결
- [ ] 변경이 프롬프트인 경우 `/interview-tester` QA 결과 첨부
- [ ] 새 트랙인 경우 rubric과 질문 가이드 모두 포함
- [ ] Korean 언어 유지 (기술 용어는 English as-is)

---

## 개발 환경

```bash
# Claude Code에서 바로 사용
claude

# 면접 시작
/interview frontend

# 프롬프트 QA
/interview-tester frontend

# 새 트랙 rubric 생성
/rubric-generator devops
```

---

## 질문이 있으시면

[Issues](../../issues)에 자유롭게 등록해주세요.
