# 기술 스택

후보 비교·조사 내용은 [reference.md](../reference.md) 참조.

## 결정 사항

| 항목 | 결정 | 결정일 | 근거 |
| --- | --- | --- | --- |
| 엔진 | Unity | 2026-10-12 | 유사작 다수 채택 (Hollow Knight, Blasphemous, Pawned Souls, Pawnbarian), 에디터·애니메이션 툴링 |
| 차원 | 2D (사이드뷰) | 2026-10-13 | 2D 소울라이크 레퍼런스 다수, 유사작(3D) 대비 차별화, 개발 부담 |
| 배포 대상 | PC (Steam) | 2026-10-13 | 소울라이크 장르 주 시장, 키보드·게임패드 조작 |
| Unity 버전 | 6.3 LTS (6000.3.x 최신 패치) | 2026-10-13 | 조사 시점 최신 LTS, 지원 2027-12까지. 6.0 LTS는 2026-10 지원 종료 |
| 렌더 파이프라인 | URP (2D Renderer) | 2026-10-13 | Built-in RP는 Unity 6.5부터 deprecated, 신규 프로젝트 비권장. URP 2D Renderer로 2D 조명·스프라이트 처리 |
| 프로젝트 위치 | 저장소 하위 `Game/` | 2026-10-13 | docs와 Unity 파일(Assets, ProjectSettings 등) 분리 |
| 버전 관리 | Git + Git LFS | 2026-10-13 | 이미지·사운드 등 바이너리 에셋 용량 관리 |

HTML + JavaScript 후보는 제외.

## 추후 검토

- Unity 6.7 LTS 출시 시 업그레이드 검토 (2026 말 예정, 조사 시점 출시 미확인)

## 프로젝트 설정 절차

Unity 설치·프로젝트 생성용 디바이스에서 실행.

1. Unity Hub 설치 (https://unity.com/download), 로그인·Personal 라이선스 활성화
2. Hub → Installs → Unity 6.3 LTS 최신 패치 설치 (Windows Build Support 기본 포함)
3. Hub → Projects → New project
   - 템플릿: **Universal 2D**
   - Project name: `Game`
   - Location: 저장소 루트 (`SoulPromotion/`)
4. 저장소 루트에 `.gitattributes` 생성 (LFS 추적 대상)

   ```gitattributes
   # 이미지
   *.png filter=lfs diff=lfs merge=lfs -text
   *.jpg filter=lfs diff=lfs merge=lfs -text
   *.jpeg filter=lfs diff=lfs merge=lfs -text
   *.psd filter=lfs diff=lfs merge=lfs -text
   *.tga filter=lfs diff=lfs merge=lfs -text
   *.tif filter=lfs diff=lfs merge=lfs -text
   *.aseprite filter=lfs diff=lfs merge=lfs -text
   # 사운드
   *.wav filter=lfs diff=lfs merge=lfs -text
   *.mp3 filter=lfs diff=lfs merge=lfs -text
   *.ogg filter=lfs diff=lfs merge=lfs -text
   # 3D
   *.fbx filter=lfs diff=lfs merge=lfs -text
   *.blend filter=lfs diff=lfs merge=lfs -text
   # 폰트
   *.ttf filter=lfs diff=lfs merge=lfs -text
   *.otf filter=lfs diff=lfs merge=lfs -text
   # 영상
   *.mp4 filter=lfs diff=lfs merge=lfs -text
   ```

5. 저장소에서 `git lfs install` 실행 (LFS hooks 설치)
6. `Game/.gitignore` 생성 — [github/gitignore Unity.gitignore](https://github.com/github/gitignore/blob/main/Unity.gitignore) 원문 사용
   - 프로젝트 생성 후 추가 (Hub가 비어 있지 않은 폴더에 프로젝트 생성을 거부할 수 있음)
   - `/` 앵커 패턴이 `Game/` 기준으로 동작
7. 확인
   - Project Settings → Editor: Asset Serialization = Force Text, Version Control = Visible Meta Files
   - `Game/Packages/manifest.json`에 `com.unity.render-pipelines.universal` 포함
   - `Game/ProjectSettings/ProjectVersion.txt`가 6000.3.x
   - `git status`에 `Game/Library`, `Game/Temp`, `Game/Logs` 미노출
   - 이미지 추가 후 `git lfs ls-files`에 표시

## 출처

- Unity 6 지원 기간 — https://unity.com/releases/unity-6/support
- Unity 6.3 LTS — https://unity.com/blog/unity-6-3-lts-is-now-available
- 렌더 파이프라인 전략 2026 — https://unity.com/topics/render-pipelines-strategy-for-2026
- Unity.gitignore — https://github.com/github/gitignore/blob/main/Unity.gitignore
