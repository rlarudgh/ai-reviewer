면접 프롬프트를 자동 QA합니다. 가상 후보자가 되어 지정 트랙의 면접을 시뮬레이션하고 품질을 검증합니다.

## 인자: $ARGUMENTS (frontend | app | server)

## 실행 단계

1. `.claude/skills/interview/prompts/{ARGUMENTS}.md` 읽기
2. `.claude/skills/interview/prompts/interviewer-system.md` 읽기
3. `.claude/skills/interview/prompts/evaluator.md` 읽기
4. `.claude/skills/interview/rubric.md` 읽기

## 시뮬레이션 규칙

토픽 가이드를 기반으로 8-12개 질문을 생성하고, 각 질문에 **다양한 수준**의 답변을 시뮬레이션:
- 2-3개: 구체적이고 깊은 답변 (senior)
- 2-3개: 적절하지만 표면적인 답변 (mid)
- 2-3개: 모호하거나 부분적으로 틀린 답변 (junior)
- 1-2개: "잘 모르겠습니다" 솔직한 답변

## QA 평가 항목

각 Q&A 페어링 대해 다음을 평가:

| 체크 항목 | 평가 기준 |
|-----------|-----------|
| 질문 난이도 | 경력자 대상에 적절한가? 정의형이 아닌가? |
| 질문 다양성 | 주제가 중복되지 않는가? 다양한 카테고리를 커버하는가? |
| 꼬리질문 논리 | 이전 답변과 자연스럽게 연결되는가? |
| 실무 관련성 | 실제 프로젝트에서 마주칠 수 있는 질문인가? |
| 심화 유도 | "왜?", "트레이드오프?", "실제 사례?"를 적절히 프로브하는가? |

## 출력

QA 리포트를 대화창에 출력하고 `docs/interviews/qa_{track}_{YYMMDD_HH:MM}.md`에 저장.

## 평가 정확도 테스트

시뮬레이션 면접을 evaluator 기준으로 자체 평가하고, 각 답변 수준의 예상 점수와 비교하여 불일치를 플래그.
