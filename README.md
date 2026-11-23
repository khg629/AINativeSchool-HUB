# AI네이티브스쿨 HUB 설치 안내

할 일마다 AI를 한 명씩 붙여 일을 맡기는 작업 공간이에요. AI네이티브스쿨 수강생용이에요.

**이 안내는 Windows 기준이에요.** 맥은 [맨 아래](#맥에서-설치하기)를 보세요.

## 시작 전에 확인하기

- **Windows 10 (1809 이상) 또는 Windows 11**, 64비트
- **Claude 유료 구독**(Pro 또는 Max). 무료 플랜으로는 Claude Code를 쓸 수 없어요.
- 인터넷이 되는 컴퓨터. 다 하면 20분쯤 걸려요.

HUB는 컴퓨터에 설치된 **Claude Code**(AI 프로그램)를 불러서 일해요. 그래서 **Claude Code를 먼저 설치하고 로그인한 다음** HUB를 설치해요.

| 순서 | 할 일 |
|---|---|
| 1 | Git 설치 |
| 2 | Claude Code 설치 |
| 3 | Claude Code 로그인 |
| 4 | HUB 설치 |
| 5 | HUB에서 연결 확인 |

---

## 1단계. Git 설치

AI가 명령을 실행할 때 쓰는 도구예요. 한 번만 설치하면 돼요.

1. [git-scm.com/download/win](https://git-scm.com/download/win)에 들어가 **Click here to download**를 눌러 설치 파일을 받아요.
2. 받은 파일을 실행하고, 설정은 바꾸지 말고 **Next**만 계속 눌러 **Install**까지 진행해요.
3. **Finish**를 누르면 끝이에요.

---

## 2단계. Claude Code 설치

1. **PowerShell 열기**: 키보드의 **Windows 키**를 누르고 `powershell`을 입력한 뒤 **Windows PowerShell**을 눌러요. (관리자 권한은 필요 없어요.)
2. 아래 명령을 복사해서 PowerShell 창에 붙여 넣고 **Enter**를 눌러요. 붙여 넣기는 **마우스 오른쪽 클릭** 또는 **Ctrl+V**예요.
   ```powershell
   irm https://claude.ai/install.ps1 | iex
   ```
3. 설치 메시지가 끝나고 다시 입력할 수 있을 때까지 기다려요.
4. **PowerShell 창을 닫고 새로 열어요.** (새 창이어야 방금 설치한 프로그램을 찾아요.)
5. 새 창에서 아래를 입력해 설치를 확인해요. `2.1.xxx (Claude Code)`처럼 버전이 나오면 성공이에요.
   ```powershell
   claude --version
   ```

> **"claude 용어가 cmdlet, 함수… 이름으로 인식되지 않습니다"가 나오면**
> 아래 두 줄을 붙여 넣고 Enter를 누른 다음, PowerShell을 닫았다 새로 열고 5번을 다시 해요.
> ```powershell
> $currentPath = [Environment]::GetEnvironmentVariable('PATH', 'User')
> [Environment]::SetEnvironmentVariable('PATH', "$currentPath;$env:USERPROFILE\.local\bin", 'User')
> ```

---

## 3단계. Claude Code 로그인

1. PowerShell에서 아래를 입력하고 Enter를 눌러요.
   ```powershell
   claude
   ```
2. 처음에는 화면 색(테마) 같은 질문이 나와요. **Enter**로 기본값을 골라 넘어가요.
3. 로그인 방법을 물으면 **Claude 구독 계정**(Claude account with subscription)을 골라요.
4. 브라우저가 열리면 Claude 계정으로 로그인하고 **승인**(Authorize)을 눌러요.
   - 브라우저가 안 열리면 PowerShell에 나온 주소를 복사해 브라우저에 붙여 넣어요.
   - 브라우저에 코드가 나오면 복사해서 PowerShell에 붙여 넣고 Enter를 눌러요.
5. PowerShell에 Claude 입력창이 나오면 로그인 성공이에요. `/exit`를 입력해 나와요.

---

## 4단계. HUB 설치

1. 아래 링크로 설치 파일을 받아요.

   ### ⬇️ [AINativeSchool-HUB-Setup.exe 받기](https://github.com/khg629/AINativeSchool-HUB/releases/latest/download/AINativeSchool-HUB-Setup.exe)

2. 받은 `AINativeSchool-HUB-Setup.exe`를 실행해요.
3. **"Windows의 PC 보호"** 파란 창이 뜨면 **추가 정보**를 누르고 **실행**을 눌러요. (코드 서명이 없어서 뜨는 경고예요.)
4. 설치 화면이 나오면 아무것도 바꾸지 말고 **다음**(또는 **설치**)을 눌러 진행하고, 마지막에 **마침**을 눌러요.
5. 시작 메뉴나 바탕화면의 **AI네이티브스쿨 HUB**를 열어요.

---

## 5단계. HUB에서 연결 확인

1. HUB 오른쪽 위 **설정**(또는 **Ctrl + ,**)을 눌러요.
2. **에이전트 기본값**의 AI 목록에서 **Claude Code**를 봐요.
   - 이름만 보이면 **연결 완료**예요.
   - **— 미설치**: HUB가 Claude Code를 찾지 못했어요. 아래 "HUB 완전히 껐다 켜기"를 해 보고, 그래도 같으면 2단계를 다시 확인해요.
   - **— 로그인 필요**: 3단계를 다시 해요.
3. 왼쪽 목록의 **✍️ 첫 일 맡겨보기**를 열고 가운데 입력창에 아무 일이나 적어 보내 보세요. AI가 답하면 모든 준비가 끝났어요. 🎉

> **HUB 완전히 껐다 켜기**
> 창의 X를 눌러도 HUB는 꺼지지 않고 작업 표시줄 오른쪽 아래(시계 옆 **^** 안)에 남아 있어요.
> 그 아이콘을 **오른쪽 클릭 › AI네이티브스쿨 HUB 종료**를 누른 다음, 다시 열어요. HUB는 켤 때 AI를 찾아요.

---

## 처음 써 보기

처음 열면 **👋 HUB 시작하기**와 **✍️ 첫 일 맡겨보기** 태스크가 들어 있어요. 시작하기 메모를 먼저 읽고, 첫 일 맡겨보기의 예시를 그대로 보내 보세요.

1. **태스크 만들기**: 왼쪽 위 "태스크 추가"에 할 일을 적고 **추가**. `#프로젝트이름`을 붙이면 그 프로젝트로 들어가요.
2. **AI에게 맡기기**: 가운데 입력창에 하고 싶은 일을 적고 보내요. AI가 일하는 동안 다른 태스크를 봐도 돼요. 끝나면 알림이 와요.
3. **작업 폴더 연결**: 태스크 위쪽 **폴더 연결**로 AI가 일할 폴더를 정해요. 연결하지 않으면 HUB 안의 태스크 전용 폴더에서 일해요.
4. **AI 고르기**: 입력창 아래에서 AI(Claude Code · Codex · Gemini)와 모델을 바꿀 수 있어요.
5. **권한**: 입력창 아래 방패 아이콘
   - **편집 허용** (기본, 권장): 파일 수정은 알아서, 위험할 수 있는 명령은 막아요.
   - **모두 허용**: 확인 없이 모든 명령을 실행해요. 믿을 수 있는 작업에만 쓰세요.
6. **AI 여러 개**: 태스크 위쪽 **+ AI 추가**로 같은 태스크에 AI를 더 붙여요. 예: Claude가 만들고 Codex가 검토. **나란히**를 누르면 대화를 옆으로 놓고 비교해요.
7. **메모**: 태스크마다 메모가 있어요. AI도 이 메모를 읽고 써요.
8. **완료**: 다 끝난 태스크는 왼쪽 동그라미를 누르거나 **완료 → 다음**을 눌러요.

---

## 팀에 맡기기

위쪽 **팀**을 누르면 세 팀이 준비되어 있어요. 팀마다 일하는 방식(팀 기억), 역할별 에이전트, 바로 쓸 수 있는 스킬이 들어 있어요.

| 팀 | 맡기면 좋은 일 | 들어 있는 스킬 |
|---|---|---|
| 🎬 콘텐츠팀 | 블로그·유튜브·SNS 글과 영상 기획 | 블로그 글 쓰기, 유튜브 대본 |
| 🔎 리서치팀 | 조사, 자료 요약, 비교표 | 시장 조사 보고서, 자료 요약 |
| 🛠 만들기팀 | 웹페이지, 반복 업무 자동화 | 랜딩페이지 만들기, 반복 업무 자동화 |

- 태스크를 팀 프로젝트(예: `#콘텐츠팀`)에 넣으면 그 팀의 방식대로 일해요.
- 어느 팀 일인지 모르겠으면 **팀 › 모든 팀**의 입력칸에 적어요. **매니저**가 알맞은 팀에 태스크를 만들어 맡겨요.
- 팀 기억, 에이전트, 스킬은 모두 고칠 수 있어요. 내 말투, 자주 쓰는 양식을 적어 둘수록 AI가 내 방식대로 일해요.
- **새 팀 만들기**로 나만의 팀을 더 만들 수 있어요.

---

## 일정 (Google 캘린더)

왼쪽 **일정비서**에게 "목요일 오후 3시 스터디 모임 잡아줘"처럼 말하면 일정을 잡아 줘요. 위쪽 **일정**에서 태스크 마감과 Google 일정을 같이 봐요.

Google 캘린더 연결은 처음 한 번만 해요. **설정 › Google 캘린더 › 처음 연결하는 방법**을 따라 하면 돼요.
1. [Google Cloud 콘솔](https://console.cloud.google.com)에서 프로젝트를 만들고 **Google Calendar API**를 사용 설정해요.
2. **Google Auth Platform**에서 앱 이름·지원 이메일을 넣고, **테스트 사용자**에 내 Google 계정을 추가해요.
3. 클라이언트를 **데스크톱 앱** 유형으로 만들고 JSON 파일을 내려받아요.
4. HUB에서 **연결 설정 JSON 불러오기**로 그 파일을 고르고 Google 계정으로 연결해요.

---

## 더 쓰기 (선택)

- **Gmail · Notion 같은 서비스**: [claude.ai](https://claude.ai) › 설정 › 커넥터에서 연결한 뒤, HUB **설정 › 커넥터 허용**에서 켜요.
- **AI가 브라우저 쓰게 하기**: **설정 › AI 브라우저 조작**을 켜면, AI가 오른쪽 브라우저 창에서 페이지를 열고 읽고 눌러요.
- **채팅**: 위쪽 **채팅**은 가볍게 묻고 답하는 곳이에요. 일이 커지면 **태스크로 만들기**를 눌러요.

---

## 다른 AI도 쓰고 싶다면 (선택)

Claude만 있어도 HUB를 다 쓸 수 있어요. 다른 AI도 붙이고 싶을 때만 설치해요. 설치한 뒤에는 **HUB를 완전히 껐다 켜요.**

### Codex (ChatGPT Plus 이상 구독)
1. [nodejs.org](https://nodejs.org)에서 **LTS** 버전을 받아 설치해요.
2. PowerShell을 새로 열고 설치해요.
   ```powershell
   npm.cmd install -g @openai/codex
   ```
3. `codex`를 입력하고 **Sign in with ChatGPT**를 골라 ChatGPT 계정으로 로그인해요.

Windows에서는 Codex가 아직 시험 단계라 잘 안 될 수 있어요.

### Gemini (Google 계정)
1. PowerShell에서 설치해요.
   ```powershell
   irm https://antigravity.google/cli/install.ps1 | iex
   ```
2. PowerShell을 새로 열고 `agy`를 입력해 Google 계정으로 로그인해요.

---

## 자주 묻는 것

**Q. AI에게 보냈는데 아무 반응이 없어요.**
설정 › 에이전트 기본값에서 Claude Code 옆에 "미설치"나 "로그인 필요"가 있는지 보세요. PowerShell에서 `claude`를 입력해 로그인이 살아 있는지 확인하고, HUB를 완전히 껐다 켜 보세요.

**Q. PowerShell에서 "이 시스템에서 스크립트를 실행할 수 없으므로…"가 나와요.**
`npm` 대신 `npm.cmd`로 입력하면 돼요. (예: `npm.cmd install -g @openai/codex`)

**Q. "모두 허용"인데도 명령이 막혔다고 나와요.**
지우는 명령처럼 위험할 수 있는 건 AI 프로그램 자체의 안전장치가 막아요. 권한 설정과는 무관해요. AI에게 다시 시키면 보통 안전한 방식으로 고쳐서 실행해요.

**Q. 사용량은 어디서 빠지나요?**
각자의 구독에서 빠져요. Claude는 Claude 플랜, Codex는 ChatGPT 플랜, Gemini는 Google 계정 한도를 써요. HUB 아래쪽 막대에 남은 양이 보여요.

**Q. 새 버전은 어떻게 받나요?**
위 4단계 링크로 다시 받아 설치하면 돼요. 내 태스크와 메모는 그대로 남아요.

**Q. 새 모델이 안 보여요.**
설정 › 에이전트 기본값 › **AI CLI 업데이트**를 눌러요.

---

## 맥에서 설치하기

M1 이상(애플 실리콘) 맥만 지원해요. 인텔 맥은 지원하지 않아요.

1. **Claude Code 설치**: 터미널(응용 프로그램 › 유틸리티 › 터미널)을 열고 아래를 실행해요.
   ```
   curl -fsSL https://claude.ai/install.sh | bash
   ```
2. **로그인**: 터미널을 새로 열고 `claude`를 실행해 브라우저에서 로그인한 뒤 `/exit`로 나와요.
3. **HUB 받기**: [AINativeSchool-HUB-mac-arm64.zip 받기](https://github.com/khg629/AINativeSchool-HUB/releases/latest/download/AINativeSchool-HUB-mac-arm64.zip)
4. zip을 풀고 `AINativeSchool HUB.app`을 **응용 프로그램** 폴더로 옮겨요.
5. 터미널에서 아래를 한 번 실행해요. 안 하면 "손상되었기 때문에 열 수 없습니다"가 떠요.
   ```
   xattr -cr "/Applications/AINativeSchool HUB.app"
   ```
6. 앱을 열고 위 **5단계**처럼 연결을 확인해요. (설정은 **⌘ ,**, 완전히 끄기는 메뉴 막대 아이콘 › **AI네이티브스쿨 HUB 종료**)
