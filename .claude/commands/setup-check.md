---
description: 실습 환경 점검. git·gh 설치, GitHub 로그인, 샘플 프로젝트, 저장소 상태를 확인하고 부족한 것을 안내한다. "점검", "확인", "세팅 됐어?", 401/권한 오류 등에 사용.
allowed-tools: Bash, Read
---

## 환경 점검

Claude Code:
!`claude --version 2>/dev/null || echo "❌ claude 없음"`

git:
!`git --version 2>/dev/null || echo "❌ git 없음 — https://git-scm.com/downloads"`

gh CLI:
!`gh --version 2>/dev/null | head -1 || echo "❌ gh 없음 — github_setup/00_github_setup_guide.md 참고"`

GitHub 로그인:
!`gh auth status 2>&1 | grep -E "Logged in|not logged|account" | head -2 || echo "❌ 로그인 안 됨 — gh auth login"`

현재 저장소 상태:
!`git status -s 2>/dev/null && git branch --show-current 2>/dev/null || echo "(아직 git 저장소 아님)"`

샘플 프로젝트:
!`test -f sample-project/index.html && echo "✅ sample-project/index.html 있음" || echo "❌ 샘플 없음"`

## 지시

위 점검 결과를 표로 정리해 수강생에게 보여줘라. **빨간 ❌ 항목이 있으면 그것부터** 한 줄 해결책과 함께 안내한다(특히 gh 로그인이 가장 흔한 막힘 — `gh auth login` 또는 "깃허브 로그인 도와줘"). 모두 ✅면 "준비 완료! `/start` 또는 `/step 1`로 시작하세요"라고 안내하라. 친절하고 간결하게.
