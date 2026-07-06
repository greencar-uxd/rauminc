# RAUM INC — 웹사이트 리뉴얼 디자인 시안 (DRAFT)

라움아이앤씨㈜ (rauminterior.co.kr 리뉴얼) 메인 + 서브페이지 시안.
순수 HTML/CSS/JS 단일 파일 구조 — 빌드 불필요, 브라우저에서 바로 열림.

**[`index.html`](./index.html) — 전체 시안 인덱스**

## 구조

방향별 통합본 3종 (각 메인 + 서브 5페이지). 실데이터·이미지 반영판을 우세안으로 채택하고, 초안(1차)의 강점(폼 검증·CARE 프로세스·한글 세리프 등)을 이식해 단일 통합했습니다.

| 방향 | 메인 | 서브 (5종) |
|---|---|---|
| A · 미니멀 화이트 | `a.html` | `a-work` · `a-work-case` · `a-about` · `a-contact` · `a-recruit` |
| B · 레드 포인트 (#C8102E) | `b.html` | `b-*.html` (동일 5종) |
| C · 다크 프리미엄 | `c.html` | `c-*.html` (동일 5종) |

- `images/src/` — 생성 원본 PNG · `images/web/` — 웹용 JPG (`web/dark/`는 C용 저조도 그레이딩)

검증·비교 리포트: [`DESIGN-VALIDATION.md`](./DESIGN-VALIDATION.md)

## 상태 (2026-07-06)

- 이미지 4/8 반영: hero-1·2·3, card-office (AI 생성 연출 이미지, 실사진 교체 예정).
  잔여 4장(card-hotel/housing/medical, gallery-1)은 생성 후 반영 예정 — 해당 슬롯은 CSS 플레이스홀더.
- 실데이터: SINCE 2012 · 임직원 65 · 주소 등은 공개 기업정보 기준 — 클라이언트 확인 후 확정.
- `〇〇` 표기 = placeholder (전화·이메일·프로젝트 수치·업무시간 등 미확정 정보). 지어내지 않음.

## 기술 메모

- 외부 라이브러리 없음. 웹폰트는 C안의 Noto Serif KR(한글 세리프)만 CDN 로드.
- 반응형 ≤900px 햄버거 + 풀스크린 오버레이(포커스 트랩·Escape) / 히어로 6초 자동 슬라이드 (hover·focus·일시정지 버튼, `prefers-reduced-motion` 대응)
- 스크롤 리빌: IntersectionObserver (미지원·감속 모드 시 즉시 표시, `<noscript>` 폴백)
- 명도 대비 WCAG AA / `:focus-visible` / 스킵 링크 / `aria-current` / 폼 입력 16px
- GitHub Pages에 그대로 배포 가능
