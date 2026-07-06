---
description: 실습 키트의 시작점. 현재 진행 상황을 파악하고 다음 할 일 하나와 전체 커리큘럼을 안내한다. "어디서부터", "시작", "다음 뭐 해" 등에 사용.
allowed-tools: Bash, Read
---

## 현재 상태 진단

git 저장소 여부 / 현재 브랜치:
!`git rev-parse --is-inside-work-tree >/dev/null 2>&1 && echo "git 저장소 ✅ (브랜치: $(git branch --show-current 2>/dev/null))" || echo "아직 git 저장소 아님 — /step 1에서 만듦"`

원격(GitHub) 연결:
!`git remote -v 2>/dev/null | head -1 || echo "(아직 원격 없음)"`

GitHub 로그인 상태:
!`gh auth status 2>&1 | grep -E "Logged in|not logged" | head -1 || echo "(gh 미설치 또는 미확인 — github_setup 참고)"`

커밋 히스토리(최근 3개):
!`git log --oneline -3 2>/dev/null || echo "(아직 커밋 없음)"`

샘플 프로젝트:
!`ls sample-project/ 2>/dev/null || echo "(sample-project 없음)"`

## 지시

너는 월간 CMDS 18회차 "git/github 자연어 실습 키트"의 안내자다. 위 상태를 보고 **git 배경지식 없는 수강생**에게 친절하게 안내하라.

1. **환영 1~2줄**: 이 키트가 "명령어 없이 말로 git/github 쓰기" 실습장임을 짧게.
2. **현재 위치 추정**: 위 상태로 어디까지 했는지 가볍게 추정.
   - gh 로그인이 안 돼 있으면 → 먼저 `github_setup/00_github_setup_guide.md`로 로그인하라고 안내(또는 "깃허브 로그인 도와줘"라고 말하면 돕는다고).
   - git 저장소가 아니면 → `/step 1`(첫 저장소 만들기)부터 권유.
   - 이미 커밋·원격이 있으면 → 다음 단계(`/step N`)를 추정해 권유.
3. **전체 커리큘럼 표**를 한눈에 보여줘 (01~06, 각 `/step N` + "이렇게 말하면 됩니다" 예시 자연어).
4. **다음 한 걸음**을 딱 하나만 명확히 제시.

설명은 간결하게, 표와 이모지로. 한 번에 다 시키지 말고 "다음 한 걸음"에 집중. 슬래시커맨드는 외울 필요 없고 자연어로도 된다는 점을 한 번 짚어줘라.
