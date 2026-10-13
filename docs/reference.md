# 레퍼런스

유사 게임, 유사 스토리, 유사 장르의 기술 스택 조사 기록. (조사일: 2026-10-12)

엔진이 공개 자료로 확인되지 않은 경우 "미확인"으로 표기.

## 1. 유사 게임 — 체스 × 소울라이크/액션

본 프로젝트와 가장 가까운 레퍼런스.

| 게임 | 핵심 | 엔진 |
| --- | --- | --- |
| [Pawned Souls](https://devmika.itch.io/pawned-souls) (Mika, itch.io) | 폰 1기로 소울라이크 전투(공격·방패·패리·회피·회복). 적 기물이 체스 규칙대로 이동·공격. 적 전멸 시 프로모션. 3D | Unity (+ Blender, Substance) |
| [Stonemachia](https://store.steampowered.com/app/2982610/Stonemachia/) (Crossfall Games, 2026-05, PC) | 폰 Zefiro가 갑옷 해금으로 나이트·비숍·룩·퀸으로 변신. 변신마다 고유 능력. 패리·타이밍 중심 소울라이크 | 미확인 |

**시사점**
- "폰 주인공 + 소울라이크 + 기물 능력 획득" 조합은 이미 존재하는 콘셉트.
- 차별점 검토 필요 항목:
  - 기물별 왕(King of Pawn, King of Rook 등)을 보스로 두는 구조
  - 보스 처치로 능력을 흡수하는 성장 방식 (Stonemachia는 갑옷 해금 방식)
  - 최종 보스 King of King

## 2. 유사 게임 — 체스 × 로그라이크 (턴제)

| 게임 | 핵심 | 엔진 |
| --- | --- | --- |
| [Shotgun King: The Final Checkmate](https://punkcake.itch.io/shotgun-king) (PUNKCAKE Délicieux) | 샷건을 든 흑색 왕이 백 기물을 상대. Ludum Dare 50 종합 1위 | 미확인 (자체 엔진 개발 언급) |
| [Pawnbarian](https://j4nw.itch.io/pawnbarian) (j4nw) | 카드 = 기물 이동. 5x5 보드 던전. 퀸 프로모션 시 카드 강화 | Unity |
| [Once A Pawn A King](https://www.indie.io/news/chess-is-broken-once-a-pawn-a-king-launches-into-version-1-0-today) (Clover Bite, 2026) | 기물 군대를 꾸려 백색 왕의 성 공략 | 미확인 |
| [Kingbreak](https://luminosit-y.itch.io/kingbreak) (itch.io, 얼리 액세스) | 체스 6종 기물 기반 보스, 최종 보스 흑색 왕. 보스 구성이 본 프로젝트와 유사 | 미확인 |
| [Real Time Chess Roguelike](https://store.steampowered.com/app/3442410/Real_Time_Chess_Roguelike/) (Steam, 출시 예정) | 턴 대신 기물별 쿨다운. 실시간 체스 메커닉 참고용 | 미확인 |

## 3. 유사 스토리

- **《거울 나라의 앨리스》** (Lewis Carroll)
  - 앨리스가 흰색 폰이 되어 8번째 칸에 도달하면 퀸이 되는 구조.
  - 작품 앞부분의 체스 문제에서 흰색 폰(앨리스)이 9수째 퀸으로 승격, 11수째 승리.
  - 본 프로젝트의 "폰의 프로모션 여정"과 직접 대응.
- **보스 능력 흡수 구조** (일반 지식, 출처 미첨부)
  - 록맨 시리즈: 보스 처치 시 보스 무기 획득
  - 다크 소울 / 엘든 링: 보스 소울·추억을 무기·주술로 교환

## 4. 유사 장르 기술 스택 (2D 소울라이크 / 메트로배니아)

| 게임 | 엔진 | 비고 |
| --- | --- | --- |
| Hollow Knight / Silksong (Team Cherry) | Unity | 손그림 PNG 스프라이트, 단순 셰이더 기반 조명 |
| Blasphemous 1·2 (The Game Kitchen) | Unity | |
| Dead Cells (Motion Twin) | Haxe + Heaps | 자체 오픈소스 프레임워크 |

## 5. 기술 스택 후보 비교

| 항목 | Unity | HTML + JS (Phaser 3) |
| --- | --- | --- |
| 유사작 채택 | 다수 (Hollow Knight, Blasphemous, Pawned Souls, Pawnbarian) | 확인된 상용 유사작 없음 |
| 2D/3D | 모두 지원 | 2D 전용 |
| 툴링 | 에디터, 애니메이션, 에셋 스토어 | 코드 중심, 물리·입력·오디오·트윈 내장 |
| 웹 배포 | WebGL 빌드 가능, 빌드 용량·로딩 부담 | 브라우저 네이티브, 경량 |

**공통 참고 라이브러리**
- [chess.js](https://github.com/jhlywa/chess.js) — 이동 생성·검증, 체크/체크메이트 판정 TypeScript 라이브러리.
  - 실시간 액션 전투에는 표준 체스 규칙이 그대로 적용되지 않으므로, 보드 기반 요소나 기물 이동 패턴 참고 용도로 한정될 가능성.

**판단 기준** (결정은 [design/tech_stack.md](design/tech_stack.md)에서)
- 2D / 3D 여부
- 배포 대상 (웹 / PC / 모바일)
- 팀 숙련도 (C# / JS·TS)

## 6. 체스 커뮤니티 밈·격언

보스 패턴·연출·대사·업적 소재 조사. (조사일: 2026-10-13)

### 6-1. 커뮤니티 밈

| 밈 | 내용 | 활용 아이디어 |
| --- | --- | --- |
| 저격(은신) 비숍 | 피앙케토(g2·b2 등)로 폰 뒤에 숨어 최장 대각선을 겨누는 비숍. 밈보다는 전략 칼럼의 비유로 확인 | King of Bishop 은신 후 대각 광선 (GDD 반영 내용과 대응) |
| f폰 금지 | 초반 f폰 이동 시 킹 노출 → 바보의 메이트·학자의 메이트 위험. 초보 격언 | 흑색 진영의 약점 설정 / King of King 약점 연출 |
| 앙파상 (Google En Passant / Holy hell) | 초보가 앙파상을 핵으로 오해한 데서 시작. r/AnarchyChess 대표 밈, "Google en passant" → "Holy hell" 콜앤리스폰스 | King of Pawn 기믹 또는 숨겨진 반격기 |
| Il Vaticano | 2022-12 r/AnarchyChess에서 만든 가짜 특수 수 (비숍 2개가 사이 기물을 잡는 수) | 이스터에그 기술 / 보스 대사 |
| Bongcloud | e폰 후 킹을 앞으로 내미는 트롤 오프닝 | King of King 등장 연출 (왕이 직접 걸어 나옴) |
| Knook | 나이트+룩 합성 기물. 밈 변형 룰에서 프로모션 대상 | 히든 프로모션 엔딩 후보 (GDD 미결 사항 "엔딩 분기"와 연결) |
| Botez Gambit | 퀸을 실수로 공짜로 내주는 것. 스트리머 Alexandra Botez 유래 | 업적 소재 (실명 제외, 6-3 참조) |
| Sacrifice the rook (queen) | GothamChess(Levy Rozman)가 룩 희생 시 "THE ROOOOK"을 외치는 캐치프레이즈에서 확산. 최초 영상·일자 미확인. 퀸 버전은 앙파상 콜앤리스폰스의 "Queen sacrifice, anyone?" | King of Rook·Queen 보스가 소환물을 희생시키는 패턴 / 플레이어 스킬 희생 시스템 |
| 콜앤리스폰스 (New response just dropped / Actual zombie / Call the exorcist / Queen sacrifice, anyone?) | AnarchyChess 앙파상 밈에서 이어지는 댓글 연쇄. 세부 기원 미확인 | 보스·NPC 대사 참고 |
| ICBM Gambit | 퀸이 기물 희생 후 보드를 가로질러 상대 퀸을 잡는 오프닝 개그. 2020-10 Bosnian Ape Society 3D 애니메이션 영상 유래 | King of Queen 장거리 돌진 연출 |
| Martin (봇) | chess.com 최약 봇 (레이팅 250~260). "5억 판을 두고도 실력이 늘지 않음" | 튜토리얼 적·약한 잡몹 (명칭 변경, 6-3 참조) |
| Juicer | 공짜로 잡을 수 있는 기물. xQc 기원설, Hikaru Nakamura가 확산 | 처형(경직 후 일격) 판정 명칭 후보 |
| "My king can't move to c2" | 초보 질문(킹이 공격받는 칸으로 이동 불가)에서 굳어진 러닝개그 | King of King 이동 제한 기믹 |

### 6-2. 전통 격언

| 격언 | 내용 | 활용 아이디어 |
| --- | --- | --- |
| "Pawns are the soul of chess" | Philidor, 1749 『L'Analyze des Echecs』 원문 "ils sont l'âme des Echecs". 현재 영어 문구의 최초 출현은 미확인 | 제목 SoulPromotion·"소울" 재화 명칭의 근거 |
| "A knight on the rim is dim" | 가장자리 나이트는 약함. 1964년 이전부터 문헌 등장, 작자 미상 | King of Knight 약점: 아레나 가장자리 착지 시 경직 |
| "Passed pawns must be pushed" | 통과한 폰은 밀어붙여야 함 | 2칸 대시 스킬 설명문 |
| "All rook endings are drawn" | 룩 엔딩은 모두 무승부. Tarrasch·Tartakower 귀속설 모두 미확인 | King of Rook 장기전 패턴 |

### 6-3. 게임 반영 시 검토 (권리 문제)

법률 자문 아님. 상업 출시 전 USPTO·KIPRIS 상표 DB 직접 조회 및 필요 시 전문가 검토 권장.

**판단 근거**
- 게임 규칙·아이디어·메커닉은 저작권 보호 대상 아님 (US Copyright Office Circular 33, Morrissey v. Procter & Gamble)
- 이름·제목·짧은 문구·캐치프레이즈는 저작권 보호 대상 아님 (Circular 33) → 상표권은 별도 쟁점
- 실존 인물의 성명·초상·음성 상업 사용은 퍼블리시티권 쟁점
  - 국내: 부정경쟁방지법 제2조 제1호 타목, 2022-04-20 시행, "국내에 널리 알려진" 인물 요건 (조항 번호는 법령 원문 확인 필요)
- 밈 원본 이미지·영상·카피파스타 전문은 저작물 → 복제 금지, 개념만 차용

**항목별 판정**

| 판정 | 항목 | 비고 |
| --- | --- | --- |
| 사용 가능 | 체스 규칙·용어 (앙파상, 피앙케토, 캐슬링, 프로모션), 저격 비숍, f폰 금지, 전통 격언 4종 | 규칙·관용 표현. Philidor 원문은 1749년 퍼블릭 도메인 |
| 사용 가능 | Il Vaticano, Knook, "Holy hell"·콜앤리스폰스 문구, "My king can't move to c2", Juicer | 커뮤니티 창작 개념·짧은 문구. 검색 범위 내 상표 미발견 |
| 사용 가능 (조건부) | Bongcloud, ICBM Gambit | 오프닝 명칭, 상표 미발견. ICBM은 Bosnian Ape Society 영상 연출·음악 모방 금지. Bongcloud는 "bong"(대마 흡입기) 연상 가능성 인지 |
| 주의 — 실명 제외 | Botez Gambit | 실존 인물 성명 포함 → 퍼블리시티권. "퀸 증정" 등 일반 표현으로 대체 |
| 주의 — 문구만 | Sacrifice the rook (queen) | 문구 자체는 사용 가능. GothamChess(2021 상표 출원, Levy Rozman 명의) 성명·목소리·말투 모방 및 보증 암시 금지 |
| 주의 — 명칭 변경 | Martin (봇) | chess.com 캐릭터 설정. "최약 봇" 개념만 차용, 이름·설정은 자체 제작 |

### 6-4. 조사 한계

- 한국어 커뮤니티 고유 밈은 검색으로 확인되지 않음
- 상표 조회는 웹 검색 기반, USPTO·KIPRIS 공식 DB 미조회

## 출처

- Pawned Souls — https://devmika.itch.io/pawned-souls
- Stonemachia — https://store.steampowered.com/app/2982610/Stonemachia/ , https://ixbt.games/en/news/2026/05/26/v-steam-vysel-saxmatnyi-soulslike-pro-pesku-prevrashhaiushhuiusia-v-drugie-figury.html
- Shotgun King — https://punkcake.itch.io/shotgun-king , https://zatu.com/en-us/blogs/interviews/shotgun-king-interview-with-remy-devaux
- Pawnbarian — https://j4nw.itch.io/pawnbarian , https://www.gamingonlinux.com/2021/10/pawnbarian-masterfully-blends-chess-like-rules-with-a-puzzle-roguelike
- Once A Pawn A King — https://www.indie.io/news/chess-is-broken-once-a-pawn-a-king-launches-into-version-1-0-today
- Kingbreak — https://luminosit-y.itch.io/kingbreak
- Real Time Chess Roguelike — https://store.steampowered.com/app/3442410/Real_Time_Chess_Roguelike/
- 거울 나라의 앨리스 — https://standardebooks.org/ebooks/lewis-carroll/through-the-looking-glass/john-tenniel/text/single-page , https://www.milibrary.org/node/315052
- Hollow Knight — https://unity.com/case-study/hollow-knight
- Blasphemous — https://en.wikipedia.org/wiki/Blasphemous_(video_game) , https://en.wikipedia.org/wiki/Blasphemous_2
- Dead Cells — https://deadcells.wiki.gg/wiki/Development
- Phaser vs Unity — https://dinogame.gg/blog/phaser-vs-unity-vs-godot-browser/ , https://en.wikipedia.org/wiki/Phaser_(game_framework)
- chess.js — https://github.com/jhlywa/chess.js
- 저격 비숍 — https://www.chess.com/blog/NetoVelazquez/the-sniper-bishop , https://www.chess.com/terms/fianchetto-chess
- f폰 금지 — https://www.uschess.org/index.php/beta-leftovers/Openings.html , https://chessfox.com/?p=21069 , https://lichess.org/@/BigBlunderGuy/blog/why-not-to-move-your-f-pawn/SB3sao1h
- 앙파상 밈 — https://knowyourmeme.com/memes/en-passant-google-en-passant , https://knowyourmeme.com/memes/what-do-i-do-in-this-position
- Il Vaticano — https://knowyourmeme.com/editorials/what-is-the-rare-chess-move-il-vaticano-the-reddit-certified-special-move-explained , https://www.houseofstaunton.com/blogs/chess-tutorials/the-ii-vaticano-chess-move-its-not-real-what-is-it
- Bongcloud — https://knowyourmeme.com/memes/bongcloud-attack , https://en.wikipedia.org/wiki/Bongcloud_Attack
- Knook — https://chess.com/blog/YEAT/look-its-a-knook
- Botez Gambit — https://www.chess.com/terms/botez-gambit-chess
- Sacrifice the rook — https://thewolfpacket.org/9982/2022-2023/why-everyone-is-playing-chess , https://www.chess.com/club/da-roooook-1
- 콜앤리스폰스 — https://mlmym.lemmy.dbzer0.com/post/16127
- ICBM Gambit — https://knowyourmeme.com/memes/icbm-gambit
- Martin 봇 — https://www.chess.com/news/view/martin-chess-bots , https://www.chess.com/news/view/halloween-bots-2023
- Juicer — https://www.chess.com/article/view/speak-like-a-chess-player
- Pawns are the soul of chess — https://chesshistory.com/winter/extra/soul.html , https://www.chess.com/article/view/are-pawns-the-soul-of-chess
- A knight on the rim is dim — https://barrypopik.com/blog/a_knight_on_the_rim_is_dim_chess_adage , https://en.chessbase.com/post/chess-sayings-and-songs
- All rook endings are drawn — https://chesshistory.com/winter/extra/rookendgames.html
- 저작권 비보호 대상 — https://www.copyright.gov/circs/circ33.pdf
- GOTHAMCHESS 상표 출원 — https://trademark.justia.com/owners/levy-rozman-4853605
- 부정경쟁방지법 퍼블리시티권 — https://www.lawtimes.co.kr/news/174433 , https://www.hwawoo.com/newsletter/2023_06_27/230627_kor_t.pdf
