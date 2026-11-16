> 이 파일의 역할: 전시해설 일정찾기 홍보 모션 영상의 **화면 규격·색·글꼴·배경 규칙·사용 소스**를 정하는 기준표입니다.

# design.md — 전시해설 일정찾기 홍보 영상

- 피그마 링크: https://www.figma.com/design/iICtp4r7wLJJ0eTOV8Xf9c/%EA%B3%B5%EA%B3%B5%EA%B8%B0%EA%B4%80-%EA%B0%9C%EC%84%A0?node-id=1021-2551 (섹션 `Mobile`, node `1021:2551`)
- 색·글꼴 값은 Figma 변수와 `src/styles/tokens.css`에서 그대로 가져왔습니다.

---

## 1. 화면 규격

| 항목 | 값 | 비고 |
|---|---|---|
| 해상도 | 1080 × 1920 (세로 9:16) | 요청서 예시값 기준 [확인 필요] |
| 프레임 | 30fps | 요청서 예시값 기준 [확인 필요] |
| 길이 | 15초 | 요청서 예시값 기준 [확인 필요] |
| 확대 비율 | Figma 360px → 영상 1080px = **3배** | 아래 글자 크기는 모두 이 비율로 계산 |
| 안전 영역 | 위·아래 각 192px, 좌우 96px 안쪽에 글자 배치 | SNS 앱 UI에 가리지 않게 |
| 게시처 | — | [확인 필요] (유튜브 쇼츠 / 인스타그램 릴스 / 기타) |

---

## 2. 브랜드 컬러

| 이름 (토큰) | HEX | 용도 |
|---|---|---|
| 흰색 `--bg-base` | `#FFFFFF` | 기본 배경, 밝은 장면 글자 뒤 바탕 |
| 먹색 `--text-main` | `#151515` | 제목·자막 글자, 어두운 배경 |
| 회색 `--text-sub` | `#5C5C5C` | 부제, 보조 설명 |
| 연회색 `--btn-main-hov` | `#EBEBEB` | 보조 배경, 목록 선택 행 |
| 중간회색 `--border-base` | `#A1A1A1` | 구분선만 (글자색 금지 — 대비 부족) |
| 진파랑 `--text-secondary` | `#002DE0` | 숫자·키워드 강조 글자 ("총 2건") |
| 파랑 `--border-primary` | `#00AAFF` | 운영일 테두리, 포커스 링 |
| 하늘색 `--btn-primary` | `#9CDEFF` | 강조 버튼, 시간 배지 |
| 분홍 `--border-secondary` | `#FF7D7F` | 휴관일 테두리, 안내 박스 테두리 |
| 연분홍 `--bg-info` | `#FFDFE0` | 휴관 안내 배경, 장소 배지 |
| 빨강 `--text-primary` | `#DD0000` | 꼭 필요한 경고 글자에만 |
| 반투명 흰색 `--bg-blur` | `#FFFFFF` 50% | 이미지 위 자막 패널 (+흐림 10) |

---

## 3. 글꼴

글꼴은 **Pretendard** 하나만 씁니다.

| 굵기 | 파일 |
|---|---|
| Regular 400 | `src/fonts/Pretendard-Regular.woff2` |
| Medium 500 | `src/fonts/Pretendard-Medium.woff2` |
| SemiBold 600 | `src/fonts/Pretendard-SemiBold.woff2` |

### 글자 크기 (Figma 스타일 × 3배)

| 용도 | 기준 Figma 스타일 | 크기 / 행간 | 굵기 |
|---|---|---|---|
| 메인 카피 | `Heading/Title` 24/36 | 72px / 108px | SemiBold 600 |
| 서브 카피 | `Heading/Sub` 20/30 | 60px / 90px | Medium 500 |
| 자막 | `Body/Main` 16/24 | 48px / 72px | Medium 500 |
| 라벨·배지 | `Card/Categori` 14/21 | 42px / 63px | Medium 500 |
| 출처·작은 글씨 | `Footer/Small` 12/18 | 36px / 54px | Regular 400 |

- 자막은 한 줄 14자 이내, 최대 2줄입니다. 화면에서 36px보다 작은 글자는 쓰지 않습니다.

---

## 4. 장면 배경색 규칙

| 장면 성격 | 배경 | 글자 | 비고 |
|---|---|---|---|
| 기본 (화면 소개) | `#FFFFFF` | `#151515` | 폰 목업 바깥 바탕 |
| 보조·구간 전환 | `#EBEBEB` | `#151515` | 흰 화면이 이어질 때 구분용 |
| 휴관·안내 | `#FFDFE0` | `#151515` | 빨강 글자 대신 먹색 유지 |
| 강조 (핵심 기능) | `#9CDEFF` | `#151515` | 장면 하나에만 쓰기 [확인 필요] |
| 오프닝·엔딩 | `#151515` | `#FFFFFF` | 로고는 흰색 버전 필요 [확인 필요] |

- 한 장면에는 배경색 하나만 씁니다. 그라데이션은 쓰지 않습니다.

---

## 5. 반복 모티프

| 모티프 | 모양 (Figma 기준 × 3) | 쓰는 곳 |
|---|---|---|
| 포커스 링 | `#00AAFF` 테두리 9px(3px×3), 모서리 12px | "누르는" 순간 표시 (손가락 그림 대신) |
| 달력 칸 | 테두리 칸 3종: 파랑 `#00AAFF` 운영 / 분홍 `#FF7D7F` 휴관 / 회색 면 `#EBEBEB` 선택불가 | 날짜 상태 소개, 장면 전환 패턴 |
| 단계 배지 | `#002DE0` 원 + 흰 숫자 1·2·3 | 자막 왼쪽 고정 위치 |
| 알약 버튼 | 완전 둥근 모서리(`Radius/LX` 999) + 입체 그림자(`Base`) | 조회하기·선택·CTA |
| 겹꺾쇠 《 》 | 전시명 괄호 | 메인 카피 강조 장식 |
| 이중 화살표 ≫ | 미술관 목록 화살표 (`icon-more-base.png`) | "다음으로" 표시 |

---

## 6. 사용할 소스 목록

### 6-1. 화면 캡처 (Figma에서 PNG로 내보내기)

아직 내보낸 파일이 없습니다. 파일명은 제안값입니다 [확인 필요]. 3배(@3x)로 내보냅니다.

| 파일명 (제안) | Figma 프레임 | node |
|---|---|---|
| `screen-main.png` | Mobile-Main (상단부) | `1021:2709` |
| `screen-menu.png` | NAV-03 (전시해설 펼침으로 추정) | `1021:2580` [확인 필요] |
| `screen-search.png` | Mobile-Search | `1021:2622` |
| `screen-select-list.png` | Select-List | `1021:2696` |
| `screen-calendar.png` | Calendar | `1021:2783` |
| `screen-search-error.png` | Mobile-SearchError | `1021:2681` |
| `screen-result.png` | Mobile-Result | `1021:2648` |
| `screen-detail.png` | Mobile-DetailPage | `1021:2656` |
| `screen-share.png` | ShareList | `1021:2705` |
| `screen-notice.png` | Notice-Popup | `1021:2785` |
| `screen-exhibition-info.png` | Exhibition-Info | `1021:2707` |

### 6-2. 로고

| 파일 | 내용 | 비고 |
|---|---|---|
| `src/assets/images/logo.png` | 서울시립미술관 / SEOUL MUSEUM OF ART (검정) | 기관 로고 사용 허락 [확인 필요] |
| — | 흰색 로고 (어두운 배경용) | 파일 없음 [확인 필요] |
| `src/assets/images/logo-wa-mark.png` | 푸터 인증 마크 | 영상 사용 여부 [확인 필요] |

### 6-3. 이미지

| 파일 | 내용 | 비고 |
|---|---|---|
| `src/assets/images/display-01.jpg` ~ `display-08.jpg` | 메인 전시 슬라이드 사진 | 실제 미술관 자료 — 사용 허락 [확인 필요] |
| `src/assets/images/detail-sample.jpg` | 상세 페이지 전시 포스터 | 사용 허락 [확인 필요] |
| `src/assets/images/museum-01.jpg` ~ `museum-08.jpg` | 분관 건물 사진 | 사용 허락 [확인 필요] |
| `src/assets/images/card-sample.jpg` | 카드 샘플 이미지 | 사용 여부 [확인 필요] |

### 6-4. 아이콘

| 파일 | 쓰는 곳 |
|---|---|
| `src/assets/icons/icon-calendar.png` | 날짜 선택 강조 |
| `src/assets/icons/icon-reset.png` | 초기화 강조 |
| `src/assets/icons/icon-search.png` | 조회 강조 |
| `src/assets/icons/icon-link.png`, `icon-link-lg.png` | 공유(링크 복사) 강조 |
| `src/assets/icons/icon-more-base.png` | ≫ 모티프 |
| `src/assets/icons/icon-menu.png` | 메뉴 진입 |

### 6-5. 소리

| 항목 | 파일 | 비고 |
|---|---|---|
| 배경음 | — | 음원 미정 [확인 필요] |
| 효과음 | — | 사용 여부 미정 [확인 필요] |

---

## 7. 확인 필요 모음

| # | 항목 |
|---|---|
| 1 | 길이·해상도·fps를 요청서 예시값(15초 / 1080×1920 / 30fps)으로 확정할지 |
| 2 | 게시처 |
| 3 | 화면 캡처 파일명과 내보내기 담당 |
| 4 | 메뉴 장면에 쓸 NAV 프레임 (세 번째 메뉴가 펼쳐진 NAV-03으로 추정) |
| 5 | 로고·전시 사진·포스터의 영상 사용 허락, 흰색 로고 파일 |
| 6 | 하늘색 강조 배경과 먹색 오프닝·엔딩 배경을 쓸지 |
| 7 | 배경음·효과음 |
