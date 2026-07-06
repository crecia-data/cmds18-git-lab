---
description: 지정한 번호의 가이드(guides/0N_*.md)를 함께 진행한다. "/step 1", "1단계 하자", "다음 단계", "step 3" 등에 사용.
allowed-tools: Bash, Read
argument-hint: "[단계 번호 1~6]"
---

## 가이드 목록

!`ls guides/ 2>/dev/null || echo "(guides 비어있음)"`

요청한 단계: $ARGUMENTS

## 지시

1. `$ARGUMENTS`(번호)에 해당하는 `guides/0N_*.md` 파일을 **Read로 읽어** 내용을 파악한다. 번호가 없으면 어떤 단계를 할지 물어보고 커리큘럼(01~06)을 보여준다.
2. 그 가이드를 **수강생과 함께 한 걸음씩** 진행한다. git 배경지식이 없다고 가정하고, 개념은 비유로 짧게 설명한 뒤 **실제로 Claude가 git/gh를 실행**해 보여준다.
3. 수강생이 자연어로 말하면(예: "되돌려줘") 해당 슬래시커맨드 동작(`/save`·`/undo`·`/experiment`·`/ship`·`/site`)으로 처리한다.
4. 한 단계가 끝나면 **다음 단계 하나만** 권한다(예: "잘했어요! 다음은 `/step 2`예요").

CLAUDE.md의 git 안전 거버넌스(위험 전 커밋·main 직접 push 금지·force push 금지)를 항상 지켜라.
