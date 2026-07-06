---
description: 변경을 바로 반영하지 않고, 검토용 PR(Pull Request)로 올린 뒤 사람이 확인하고 머지한다. "검토받게 올려줘", "PR 만들어줘", "바로 반영 말고", "반영해줘"(머지) 등에 사용.
allowed-tools: Bash
---

## 현재 상태

브랜치 / 변경 / 원격:
!`git branch --show-current 2>/dev/null; git status -s 2>/dev/null; git remote -v 2>/dev/null | head -1`

로그인:
!`gh auth status 2>&1 | grep -E "Logged in|not logged" | head -1`

## 지시

너는 "**에이전트는 PR로 제출, 사람이 승인**"이라는 Human-in-the-loop을 수강생이 체험하게 한다. 결재 올리기 비유를 활용하라.

1. **로그인·원격 확인**: gh 로그인 안 됐으면 `github_setup` 안내. 원격(GitHub repo)이 없으면 먼저 `/step 1`로 올리게 안내.
2. **현재 브랜치가 main이면** → 먼저 브랜치로 옮기라고 안내(`/experiment`). **main에 직접 push/커밋하지 않는다**(가드레일).
3. 변경 커밋 후 브랜치를 push: `git push -u origin <브랜치>`.
4. **PR 생성**: `gh pr create --title "<한국어 제목>" --body "<무엇을 왜 바꿨는지 요약>"`. 생성된 PR URL을 알려준다.
5. **"뭐가 바뀌어?"** 류 질문엔 `gh pr diff` 또는 `git diff main...<브랜치>`를 사람 말로 요약해 보여준다("색이 빨강→파랑, 소개문구 1줄 추가").
6. 수강생이 **"반영해줘"**라고 하면 → `gh pr merge --merge`(또는 squash)로 머지하고, "✅ 사람이 검토하고 승인해서 main에 반영됐어요"라고 마무리. main으로 전환·pull까지 안내.

핵심 메시지: "AI가 만든 변경도 **바로 main에 들어가지 않고, 당신이 PR을 보고 승인**해야 반영됩니다."
