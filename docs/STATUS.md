# STATUS

갱신일: 2026-10-14

## 현재 단계

기획 단계. 핵심 설계 확정, 프로토타입 착수 전.

## 확정 사항

| 항목 | 내용 | 상세 |
| --- | --- | --- |
| 엔진 | Unity 6.3 LTS / URP 2D Renderer | [tech_stack.md](design/tech_stack.md) |
| 차원·플랫폼 | 2D 사이드뷰 / PC (Steam) | [tech_stack.md](design/tech_stack.md) |
| 아트 | 흑백 모노크롬 + 포인트 컬러 (픽셀 아트 전환 가능성 보류) | [GDD 1장](design/game_design.md#1-개요) |
| 전투 | 실시간 액션, 3타 콤보·구르기·가드/퍼펙트 가드, 스태미나 기반 | [GDD 3장](design/game_design.md#3-전투) |
| 보스 | King of Pawn → Knight → Bishop → Rook → Queen → King of King | [GDD 4장](design/game_design.md#4-보스흡수-스킬) |
| 성장 | 보스 스킬 흡수, 슬롯 2개, 머티리얼로 레벨업(스탯 1개 선택, 목표 약 Lv30) | [GDD 5장](design/game_design.md#5-성장-시스템) |
| 소울라이크 | 머티리얼 드롭형 사망 패널티, 체크포인트 = 체스 시계 | [GDD 6장](design/game_design.md#6-소울라이크-규칙) |
| 스테이지 | 랭크 = 스테이지, 선형 진행 | [GDD 7장](design/game_design.md#7-월드스테이지) |
| 튜토리얼 | 랭크 2, 환경 표식 안내, 강제 사망 이벤트로 마무리 | [GDD 7장](design/game_design.md#7-월드스테이지) |
| 일반 적 | 누적형 구성, 체스 규칙은 공격에만 반영 | [GDD 7장](design/game_design.md#7-월드스테이지) |
| 엔딩 | 퀸 단일 엔딩, 다중 분기 확장 가능 구조 | [GDD 8장](design/game_design.md#8-스토리세계관-초안-확정) |

## 미결 사항

- 보스 패턴·스킬 밸런스 수치 (King of Pawn·전방 대시는 초안 작성, [GDD 9장](design/game_design.md#9-프로토타입-범위))

## 다음 단계

1. Unity 프로젝트 생성 및 버전 관리 설정 — 개발 PC에서 진행 ([절차](design/tech_stack.md#프로젝트-설정-절차))
2. 프로토타입: 기본 조작 → King of Pawn 전투 → 전방 대시 흡수 ([GDD 9장](design/game_design.md#9-프로토타입-범위))
