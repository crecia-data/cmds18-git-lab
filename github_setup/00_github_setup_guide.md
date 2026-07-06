# 🐙 GitHub 준비 가이드 (계정 + gh 로그인)

> 이번 실습은 **실제 GitHub에 올리고(push)·검토(PR)·배포(Pages)**까지 직접 합니다.
> 그래서 ① GitHub 계정과 ② `gh` 로그인이 필요합니다. 5분이면 됩니다. 막히면 Claude에게 **"깃허브 로그인 도와줘"**라고 하세요.

---

## 1단계 — GitHub 계정 (있으면 건너뛰기)

- 가입: https://github.com/signup
- 이메일·비밀번호·사용자명(=내 GitHub 아이디)만 정하면 끝. (무료)

## 2단계 — `gh` CLI 설치 (있으면 건너뛰기)

확인: 터미널에 `gh --version`
- 없으면 설치:
  - **macOS**: `brew install gh`
  - **Windows**: `winget install --id GitHub.cli` (또는 https://cli.github.com)
  - 기타: https://github.com/cli/cli#installation

## 3단계 — 로그인 (핵심!)

터미널에 다음 한 줄:
```bash
gh auth login
```
그러면 몇 가지를 물어봅니다. **이렇게 고르면 됩니다:**

| 질문 | 선택 |
|------|------|
| What account? | **GitHub.com** |
| Preferred protocol? | **HTTPS** |
| Authenticate Git with your GitHub credentials? | **Yes** |
| How to authenticate? | **Login with a web browser** (가장 쉬움) |

→ 화면에 **one-time code**(예: `AB12-CD34`)가 뜹니다. Enter를 누르면 브라우저가 열리고, 그 코드를 입력 → 승인하면 끝.

> 💡 **더 쉬운 방법**: Claude에게 *"깃허브 로그인 도와줘"*라고 하면 위 과정을 같이 진행해 줍니다.

## 4단계 — 확인

```bash
gh auth status
```
→ `✓ Logged in to github.com account [내아이디]` 가 보이면 성공!
또는 Claude에게 **`/setup-check`** 라고 입력하면 한 번에 점검해 줍니다.

---

## 🆘 자주 막히는 점

- **`gh: command not found`** → 2단계(설치)를 안 했습니다.
- **브라우저 코드 입력이 안 먹혀요** → 코드 대소문자·하이픈까지 정확히. 시간이 지나면 만료되니 `gh auth login`을 다시.
- **회사 노트북이라 설치가 막혀요** → 강의 중 강사/조교에게 말씀해 주세요(대안 안내).

준비되면 → 실습 폴더에서 `claude` 실행 → `/start` 🎬
