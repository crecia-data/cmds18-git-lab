---
description: 내 프로필 페이지를 GitHub Pages로 무료 웹 배포한다. "사이트로 띄워줘", "웹에 올려줘", "링크 만들어줘", "사람들한테 보여주게", "배포해줘" 등에 사용.
allowed-tools: Bash
---

## 현재 상태

원격 저장소 / 공개여부:
!`gh repo view --json name,visibility,url 2>/dev/null || echo "(아직 GitHub 저장소 없음 — /step 1 먼저)"`

## 지시

너는 수강생의 `sample-project/`(프로필 1페이지)를 **GitHub Pages로 무료 공개**하도록 돕는다.

1. **무료 조건 안내**: GitHub Pages는 **공개(public) 저장소면 무료**다. 저장소가 private이면 → public 전환이 필요함을 안내(또는 Pro 플랜). 수강생에게 공개해도 되는지 한 번 확인.
2. **index.html 위치 확인**: Pages는 보통 저장소 루트 또는 `/docs`의 `index.html`을 발행한다. 이 키트는 `sample-project/index.html`이므로, ① 루트로 옮기거나 ② Pages 소스 폴더를 맞추도록 안내(가장 간단한 방법을 골라 실행).
3. **Pages 활성화**: `gh api`로 Pages를 켜거나(`gh api -X POST repos/{owner}/{repo}/pages -f source...`), 안내 메시지로 저장소 Settings→Pages에서 브랜치를 고르게 돕는다. (gh로 안 되면 웹 UI 단계를 친절히 안내)
4. **결과 URL 안내**: 배포 URL(`https://<id>.github.io/<repo>/`)을 알려주고, "반영까지 1~2분 걸릴 수 있어요"라고 안내.
5. 마무리: "🌐 이제 이 링크를 누구에게나 보낼 수 있어요. 공개 저장소라 Pages·Actions 다 무료입니다."

⚠️ 수치/절차는 강의 시점 GitHub UI에 따라 다를 수 있으니, 막히면 Settings→Pages 화면을 함께 보며 진행하라.
