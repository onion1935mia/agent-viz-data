# agent-viz-data

에이전트 활동 시각화 화면이 읽는 이벤트 데이터. 공개 저장소다.

- 들어가는 것: 에이전트 별칭, 방(저장소 이름), 시작·끝 시각, 결과, 종류, 동작 종류(desk, search, mcp, talk, record, report, chat), 대화 상대 에이전트 별칭, 채팅 창구(chat, cowork)와 결과(answer, record, ask). 작업 내용 문구, 검색어, 파일 이름, 대화 내용은 넣지 않는다.
- 만드는 곳: 비공개 저장소의 수집기. 사람이 직접 고치지 않는다.
- 보여주는 곳: sapling 사이트의 에이전트 사무실 화면.

## 파일 (형식 0.3부터)

| 파일 | 내용 |
|---|---|
| `index.json` | 날짜 목록 `days`와 `generated_at`. 새 이벤트가 없어도 10분마다 `generated_at`이 새로 올라온다(수집기가 살아 있다는 표시) |
| `events/YYYY-MM-DD.json` | 한국 날짜 기준으로 그날 시작한 이벤트. 최근 30일치 |

- 읽는 주소: `https://raw.githubusercontent.com/onion1935mia/agent-viz-data/main/` 아래 위 파일들. 읽기 전용이다.
- 파일 하나는 500KB 이하, 하루 파일은 1500건 이하다.
- 30일보다 오래된 날짜 파일은 지우지 않고 남아 있다. 화면은 30일까지만 읽는다.
