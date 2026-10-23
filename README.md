# 샤이니 사무실 키트

AI 직원한테 일을 시키면, 3D 사무실에서 로봇 직원들이 그 일을 하는 게 실시간으로 보이는 스킬.
처음 설치하면 실장이 내가 하는 일을 물어보고, 거기에 맞는 직원과 업무 매뉴얼을 만들어 준다.

**데모 (설치 없이 보기):** https://shineonyou1274.github.io/shiny-office-kit/

**자세한 사용법 (블로그):** https://blog.naver.com/shineonyou4ever/224450426761

## 설치

### AI한테 한 줄 (제일 쉬움)

Aside나 Claude Code 채팅창에 이렇게 쓰면 된다.

```
https://github.com/shineonyou1274/shiny-office-kit 이 스킬 설치해줘
```

AI가 아래 git clone을 대신 해 준다. 스킬 폴더 안에 `shiny-office` 라는 이름으로 넣는 게 전부다. 설치가 끝나면 "사무실 열어줘"라고 하면 된다.

### 직접 git clone

Claude Code

```
git clone https://github.com/shineonyou1274/shiny-office-kit ~/.claude/skills/shiny-office
```

Aside (Windows)

```
git clone https://github.com/shineonyou1274/shiny-office-kit "%USERPROFILE%\.aside\u\0\skills\user\shiny-office"
```

git이 없으면 위쪽 초록색 **Code → Download ZIP** 으로 받아서, 같은 위치에 `shiny-office` 폴더로 풀면 된다.

### 맥(macOS)에서

- 맥에는 git이 없는 경우가 많다. 그때는 위의 **Download ZIP** 으로 받아 스킬 폴더에 `shiny-office` 이름으로 넣으면 된다. AI한테 "이 스킬 설치해줘"라고 하면 자기 스킬 폴더를 찾아 알아서 넣는다.
- 이 문서와 매뉴얼의 경로는 윈도우 기준(`\`)으로 적혀 있다. 맥에서는 `/`로 읽으면 된다. AI가 알아서 바꿔 주지만, 사무실 화면이 안 움직이면 `status.js` 경로의 `\`를 `/`로 고쳐 달라고 하면 된다.
- 사무실 화면은 크롬이 아니어도 된다. 사파리든 Aside 브라우저든 3D(WebGL)가 되는 브라우저에서 `office.html`을 열면 된다.
- 맥 설치기(첫 사용자 민티님): https://m.blog.naver.com/leezmagnificent/224450865121

## 첫 출근

1. 채팅창에 **"사무실 열어줘"**
2. 실장이 다섯 가지를 한 번에 묻는다: 호칭, 하는 일, 자주 맡길 일, 블로그·채널, 말투
3. 답하면 직원 명부를 제안한다. 이름이나 일을 바꾸고 싶으면 말하고, OK하면 끝
4. 직원 매뉴얼(`staff\`)과 사무실 화면 설정(`config.js`)이 자동으로 만들어진다
5. `shiny-office` 폴더의 `office.html` 을 브라우저(크롬·사파리·엣지, 3D가 되면 아무거나)로 열어 두고 "하나야, ~해줘"처럼 부르면 된다

직원을 바꾸고 싶으면 언제든 "직원 바꿔줘".

## 어떻게 움직이나

- `SKILL.md` 는 업무 매뉴얼이다. 직원 이름을 부르면 AI가 이걸 먼저 읽고 그 직원 역할로 일한다.
- AI는 단계가 바뀔 때마다 `status.js` 에 "지금 누가 무엇을 하는지" 적는다.
- `office.html` 은 4초마다 그 메모를 읽어 로봇을 움직인다. 화면은 보여주기만 하고, 일은 채팅창에서 시킨다.
- 직원은 발행, 업로드, 댓글을 하지 않는다. 결과는 임시저장이나 파일까지. 올리는 건 사람이 한다.

## 업데이트

채팅창에 "사무실 업데이트해줘" 또는 폴더에서 `git pull`. 내 설정(`my-office.md`, `config.js`, `staff\`)은 그대로 남는다.

## 라이선스

[CC BY-NC-SA 4.0](LICENSE). 깃허브에서 Fork하면 출처는 자동으로 남는다.
깃허브 밖(블로그, 카페, 연수 자료 등)에 올리거나 고친 버전을 나눌 때만 이 한 줄을 남겨 주면 된다.

```
원본: 샤이니 사무실 키트 by shiny-peace (@shiny.vibe_logic) https://github.com/shineonyou1274/shiny-office-kit
```

판매하거나 유료 강의 자료로 쓰는 건 안 된다. 사무실 화면 아래 "made by shiny-peace" 표시는 지우지 말아 주세요.
3D 화면에 쓴 three.js는 MIT 라이선스 (`LICENSE-three.txt`).
