# MEMORY.md — 현재 상태와 결정 기록

이 파일은 살아있는 상태 문서다. 카드가 바뀌거나 결정이 내려질 때마다 갱신한다. 규칙은 `AGENTS.md`, 평가 상세는 `EVALUATION.md`에 있다.

갱신일: 2026-07-17

## 현재 상태

- **산출물 위치 이동**: 발행본은 이제 `docs/index.html` (GitHub Pages용 docs 폴더). assets도 `docs/assets/`로 이동. 과거 Nintendo 스타일 원본과 airbnb/discord 실험본은 `archive/`로 이전(로고 경로 깨짐, 보관용).
- **디자인 전면 교체**: "The Patchbay" — 정밀 계측 장비(패치베이) 콘셉트, **라이트 모드**. IBM Plex Sans KR + Plex Mono. 시그니처 = 히어로 우측 커넥터 스펙트럼(카테고리별 카드 수 세그먼트 LED 미터, 클릭 시 섹션 점프). PINK(UIUX)/GOLD(리더) 평가로 폴리시: 아바타 실패 시 이니셜 폴백, "자주 찾는" 한글 라벨, 스티키 서브메뉴 상단 밀착(top:0) + 클릭 시 섹션 제목 노출 스크롤 보정.
- 카드 **60건**, 10개 카테고리: 법률·특허 7 / 금융·투자 11 / 경제·통계 5 / 부동산 3 / 지도·교통 5 / 검색·리서치 5 / 생활·여행 13 / 채용·HR 3 / 영업·CRM 3 / 문서·협업 5
- federal-register-mcp(미국 연방관보 ★0) 제거 → 60. 미국 법률은 us-legal-mcp가 커버(중복 정리).
- 푸터 로고: `logo1-transparent.png`(주황). 라이트 배경에서 흰색 로고가 안 보여 교체.
- 스타·포크 기준일: 2026-07-16 (기존), 신규 9건은 2026-07-17 실측
- UI 현황: 세로형 카드 그리드(auto-fill), 스타순 고정, 퀵픽 토글, 인증 LED 범례("구분"), 스티키 채널바(top:0), 스크롤스파이, 플로팅 맨 위로

## 정본 분기 주의

정본 `index.html`(현재 `archive/`)과 발행본 `docs/index.html`의 카드 구성이 다르다. AGENTS.md의 선정 기준·표기 원칙은 유효하지만, "산출물 = 루트 index.html" 전제는 `docs/index.html`로 갱신 필요(사용자 승인 시 AGENTS.md 반영).

## 카드 교체 이력 (2026-07-17, docs/index.html)

- **원칙 추가**: 클로드가 기본 커넥터로 이미 연결한 유명 글로벌 SaaS는 등재하지 않는다. 이 카탈로그의 가치는 따로 찾지 않으면 모르는 한국·틈새 커넥터. (사용자 지시)
- **제거 8건**: Notion·Figma·PowerPoint·Excel(클로드 기본 커넥터/스킬), LS증권 ★2·서울시 be-node ★1·한국은행 ECOS ★1(korea-finance가 커버)·지하철 k-targo ★1·네이버웍스 ★1(최저스타·중복).
- **추가 한국 틈새 4건**: 나라장터(조달청) ★0·관세청 UNI-PASS ★0·쿠팡 ★16·포트원 ★26. 신뢰할 만한 순수 공공은 조달청·관세청 2개뿐이라 나머지는 인지도 높은 한국 민간으로 채움.
- **추가 미국 5건**: QuickBooks ★318(인튜이트 공식)·Shopify ★228·Meta Ads ★1085·Reddit ★752(무인증)·Wikipedia ★270. 클로드 기본 커넥터 아닌 것으로 선별.
- **원칙 확장 적용 (2026-07-17)**: 클로드 공식 커넥터 디렉터리에 있는 Stripe·PayPal·HubSpot·Salesforce 4건 제거(65→61). LinkedIn은 공식 커넥터가 아니라 유지. (레지스트리 도구는 빈 결과라 claude.ai 커넥터 디렉터리 지식으로 판단 — 특정 건 이견 시 사용자 확인)
- 미확인 리스크: 조달청·관세청은 ★0 개인 저장소(검증 얕음).

## 확정된 결정과 이유

- **사이드바 삭제, 카드 전폭 3단** (2026-07-17). 카드가 주인공. 사이드바의 인증 안내만 범례 스트립으로 이사.
- **정렬 컨트롤 삭제, 스타순 고정**. 정렬 선택이 실익 없이 UI만 차지.
- **퀵픽 = 토글 필터**. 누르면 점등+필터, 다시 누르면 해제. 결과 건수 스트립은 이 토글이 대체해서 삭제.
- **출처 직관성 원칙으로 11건 삭제**: ODsay, Exa, Tavily, Kagi, Brave, Financial Datasets, Massive, Alpaca, Equibles, CourtListener, us-legal-tools. 상세 사유는 EVALUATION.md 6차.
- **스킬 라이브러리 반입은 기준 유지로 결정** (사용자 선택). Figma-Context-MCP 추가, 국가데이터처 소스 ★12→★76 교체.
- **airoasting/hound는 미등재**. 저장소 확인 결과 순수 스킬(plugin.json에 mcpServers 없음). 넣으려면 기준 1 예외 B를 "자사 스킬"로 개정하고 dart와 함께 묶어야 한다.
- **설명 약자 풀어쓰기** 8건 적용 (DART→금융감독원 전자공시 등).

## 보류 목록 (재검토 후보)

- 스킬 라이브러리 보류 13건. 무명 출처 3(Maverick, Octagon, GBrain), 개발자 도구 5(claude-context, Context Mode, code-review-graph, token-savior, token-optimizer), 모음집 3(공식 servers, awesome 2종), GitHub MCP Server(브랜드는 직관적, 용도가 개발자향), 이전 삭제 3건(Exa, Alpaca, Financial Datasets)은 부활 금지.
- 10점 잔여 갭 2건: 검색·퀵픽 상태의 URL 동기화(링크 공유 시 상태 보존), 칩 점프 중 스파이가 중간 섹션을 스치는 잔상.
- 제외 이력(404/비공개): workbookbulb863/korean-law-alio-mcp, ChangooLee/mcp-kr-realestate, Shopify/dev-mcp.

## 다음 스타·포크 갱신 시

`DATA` 배열의 실측값과 푸터의 기준일 문구를 함께 갱신한다. k-skill 계열(★6244 ⑂717)은 모음집 저장소 전체 값이므로 NomaDamas/k-skill 하나만 조회해서 일괄 반영한다.
