# RAUM INC — 웹사이트 리뉴얼 디자인 시안 (DRAFT)

라움아이앤씨㈜ (rauminterior.co.kr 리뉴얼) 메인 + 서브페이지 시안.
순수 HTML/CSS/JS 단일 파일 구조 — 빌드 불필요, 브라우저에서 바로 열림.

**[`index.html`](./index.html) — 전체 시안 인덱스 (1차/2차 비교)**

## 구조

### 2차 시안 (V2 — 실데이터·이미지 반영판)

| 방향 | 메인 | 서브 (5종) |
|---|---|---|
| A · 미니멀 화이트 | `a2.html` | `a2-work` `-work-case` `-about` `-contact` `-recruit` |
| B · 레드 포인트 (#C8102E) | `b2.html` | `b2-*.html` |
| C · 다크 프리미엄 | `c2.html` | `c2-*.html` |

- `images/src/` — 생성 원본 PNG · `images/web/` — 웹용 JPG (`web/dark/`는 C용 저조도 그레이딩)

### 1차 시안 (V1 — 초안, 접근성 수정 반영)

| 방향 | 메인 | 서브 (5종) |
|---|---|---|
| A · 미니멀 화이트 | `a.html` | `a-work` `-project` `-about` `-contact` `-recruit` |
| B · 레드 포인트 | `b.html` | `b-*.html` |
| C · 다크 프리미엄 | `c.html` | `c-*.html` |

검증 리포트: [`DESIGN-VALIDATION.md`](./DESIGN-VALIDATION.md)

## 상태 (2026-07-03)

- V2 이미지 4/8 반영: hero-1·2·3, card-office (AI 생성 연출 이미지, 실사진 교체 예정).
  잔여 4장(card-hotel/housing/medical, gallery-1)은 생성 후 반영 예정 — 해당 슬롯은 CSS 플레이스홀더.
- V2 실데이터: SINCE 2012 · 임직원 65 · 주소 등은 공개 기업정보 기준 — 클라이언트 확인 후 확정.
- `〇〇` 표기 = placeholder (전화·이메일·프로젝트 수치 등 미확정 정보). 지어내지 않음.

## 기술 메모

- 외부 라이브러리·웹폰트 CDN 없음 (V1 C안의 Noto Serif KR 제외)
- 반응형 ≤900px 햄버거 + 풀스크린 오버레이 / 히어로 6초 자동 슬라이드 (hover·focus 정지, `prefers-reduced-motion` 대응)
- 스크롤 리빌: IntersectionObserver (미지원·감속 모드 시 즉시 표시, `<noscript>` 폴백)
- 명도 대비 WCAG AA 기준 / `:focus-visible` / 스킵 링크 / `aria-current`
- GitHub Pages에 그대로 배포 가능
