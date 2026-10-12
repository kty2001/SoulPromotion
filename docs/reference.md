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
