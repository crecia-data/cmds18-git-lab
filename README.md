# cmds18-git-lab — 월간 CMDS 18회차 실습 키트

> **git & GitHub을 명령어 없이, Claude Code에게 말로 시켜서 쓰는 실습장.**
> 대상: git/github 배경지식이 거의 없는 분. 오늘의 약속 = **명령어 0개, 전부 자연어로.**

## 어떻게 시작하나요?
👉 **`00_START_HERE.md`** 를 먼저 읽으세요. (압축 풀고 → 이 폴더에서 `claude` 실행 → `/start`)

## 무엇을 하나요? (가이드 01~06)
1. 첫 저장소 만들기 — 내 프로필 페이지를 깃허브에 올리기
2. 저장점 & 되돌리기 — 망쳐도 되돌리는 안도감
3. 평행우주 실험(브랜치) — 원본 안 건드리고 실험
4. 검토 관문(PR) — 바로 반영 말고 검토 후 머지
5. 무료 배포(Pages) — 내 사이트를 웹에 공개
6. 규칙으로 굳히기 — 안전규칙·단축커맨드 세팅

## 폴더 구조
```
cmds18-git-lab/
├── 00_START_HERE.md      ← 여기부터!
├── CLAUDE.md             ← AI 하네스(안전규칙·자연어 매핑)
├── .claude/
│   ├── settings.json     ← 안전 권한(force push·rm 차단)
│   └── commands/         ← /start /setup-check /step /save /undo /experiment /ship /site
├── github_setup/         ← GitHub 계정·gh 로그인 가이드
├── sample-project/       ← 실습 대상: 내 프로필 1페이지(index.html)
└── guides/               ← 단계별 실습(01~06)
```

## 준비물
Claude Code · git · **GitHub 계정** · **`gh` CLI 로그인**. (자세히는 `00_START_HERE.md` / `github_setup/`)

---
*월간 CMDS · CMDSPACE · 박준 제작 (초안)*
