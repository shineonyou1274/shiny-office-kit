# 샤이니 사무실 키트

AI 직원 7명(실장 + 6명)이 3D 사무실에서 일하는 게 보이는 세팅.
직원한테 일을 시키면 실제 AI 에이전트가 일하고, 그 진행 상황이 3D 사무실 로봇으로 실시간 표시됨.

made by shiny-peace (@shiny.vibe_logic)

**바로 보기 (설치 없이 데모):** https://shineonyou1274.github.io/shiny-office-kit/

**사용법 전체 (블로그):** https://blog.naver.com/shineonyou4ever/224450426761

## 공유·변형 조건 (꼭 읽어 주세요)

키트는 무료입니다. 직접 쓰고, 고쳐 쓰는 것도 환영합니다. 대신 아래는 꼭 지켜 주세요.

1. 다른 곳에 공유할 때는 반드시 출처를 밝힌다.
   출처: 샤이니 사무실 키트 · shiny-peace (@shiny.vibe_logic) · https://blog.naver.com/shineonyou4ever/224450426761
2. 고치거나 바꿔서 쓸 때도 마찬가지다. 직원 이름, 매뉴얼, 디자인을 바꿨더라도 출처를 남긴다. 처음부터 만든 것처럼 올리지 않는다.
3. office.html 화면 아래 "made by shiny-peace" 표시는 지우지 않는다.
4. 키트나 고친 버전을 돈 받고 팔거나 유료 강의 자료로 넣지 않는다.
5. 파일을 다시 올려 나누기보다 위 블로그 글 링크를 공유한다. 그래야 받는 사람이 사용법과 이 조건을 같이 본다.

라이선스: CC BY-NC-SA 4.0 (저작자 표시 · 비영리 · 동일조건 변경 허락)
3D 화면에 쓴 three.js는 MIT 라이선스다. LICENSE-three.txt는 지우지 않는다.
사용법 전체: https://blog.naver.com/shineonyou4ever/224450426761

## 들어 있는 것

| 파일 | 뭐임 |
|---|---|
| `office.html` | 3D 사무실. Chrome으로 열면 끝. 인터넷 없어도 열림 |
| `status.js` | 실황 파일. AI가 일하면서 덮어씀. 처음엔 예시 일감 하나 들어 있음 |
| `handoff\` | 직원끼리 결과물 넘기는 폴더 |
| `skill\shiny-office\SKILL.md` | 직원 명부 + 사무실 규칙 + 일하는 순서. AI한테 주는 매뉴얼 |
| `LICENSE-three.txt` | 3D 라이브러리 three.js 라이선스 (MIT) |

## 1. 사무실만 보기 (설치 없음)

1. 이 페이지 위쪽 초록색 **Code → Download ZIP** 으로 받아서 압축을 아무 폴더에 푼다. 예: `C:\shiny-office`
2. `office.html` 을 Chrome에 끌어다 놓는다.
3. "데모" 버튼: 일감 5개가 자동으로 돌아감. "실제 업무" 버튼: `status.js` 내용이 보임.

## 2. 직원들 진짜로 일하게 하기

필요한 것: 스킬(SKILL.md)을 읽을 수 있는 AI 에이전트. 예: Aside, Claude Code.

1. `skill\shiny-office` 폴더를 에이전트의 스킬 폴더에 복사한다.
   - Aside: `C:\Users\<내 이름>\.aside\u\0\skills\user\`
   - Claude Code: `C:\Users\<내 이름>\.claude\skills\`
2. 복사한 `SKILL.md` 의 "설정" 칸을 채운다.
   - `OFFICE_DIR` 에 1번에서 푼 폴더 경로 (예: `C:\shiny-office`)
   - 내 이름, 하는 일, 블로그/채널, 말투
3. `office.html` 을 Chrome으로 열어 둔다.
4. 에이전트한테 일 시키면 됨:
   - "레이야, 이번 주 나온 AI 신기능 중에 쓸 만한 거 골라줘"
   - "실장, 이번 주 소재 레이가 찾고 유나는 쇼츠 대본 써줘"
   - 직원 로봇을 누르면 부르는 말 예시가 나오고, 누르면 복사됨.

## 3. 내 사무실로 바꾸기

- 간판 이름: `office.html` 을 메모장으로 열고 맨 위 `OFFICE_NAME` 수정.
- 직원 이름·색·하는 일: 같은 곳 `ROLES` 수정. `SKILL.md` 명부의 이름과 똑같이 맞춰야 로봇이 움직임. `실장` 은 지우지 말 것.
- 데모 일감: `PROJECTS` 수정.

## 일하는 순서

사장님 요청 → 실장 지휘 (조사 필요한지, 누구 순서인지, 지시서) → 직원들 → 실장 검수 → 사장님 승인

- 발행, 업로드, 댓글은 직원이 안 함. 결과는 임시저장이나 파일까지만.
- 촬영처럼 내가 먼저 해야 하는 단계가 나오면 결재함에서 멈춤.

## 안 될 때

- 로봇이 안 움직임: `status.js` 가 `office.html` 과 같은 폴더에 있는지 확인. 다른 폴더면 주소 뒤에 `?status=file:///C:/경로/status.js` 를 붙여서 열기.
- 화면이 하얗게만 나옴: Chrome에서 그래픽 가속(하드웨어 가속)이 꺼져 있는지 확인.
