# ZeniManager 포트폴리오 인포그래픽 제작 기록

## 디자인 토큰 수정

- 메인: `#009C64`, 전체 배경: 흰색 `#FFFFFF`
- 보조 패널: `#F0EEE9` (사용자 입력 `FOEEE9`를 HEX로 해석)
- 라벨 모서리: small radius
- 글꼴 생성 지시: Noto Sans / Noto Sans KR. 래스터 생성 결과의 실제 글꼴 파일 일치는 미확인.
- 취소 연그레이 / 삭제 Tomato `#FF6347`: 해당 버튼이 없어 사용하지 않음
- 수정 도구: 기본 제공 image_gen, 기존 PNG를 입력으로 편집

### 수정 프롬프트

```text
Edit the supplied ZeniManager infographic. Preserve its 1536x1024 landscape composition, all three contribution illustrations, search flow steps, all Korean and English wording verbatim, their order, legibility and correct spelling. Preserve the polished soft dimensional 3D clay illustration quality. This is a visual design-token revision only, not a redesign of the information.
Apply these design tokens throughout:
- Main brand color #009C64 emerald green, replacing the current blue/turquoise as the dominant accent on counselor clothes, charts, database cylinders, search arrows, profile icons, shield, reconnect icon, headings accents and badges. Highlights may be pale green, shadows darker green. Avoid dominant blue or navy styling. Main headings use very dark charcoal green #16352A for readability.
- Entire outer canvas background PURE WHITE #FFFFFF, without a full-canvas beige/gray tint.
- Secondary panel surfaces warm off-white #F0EEE9, particularly bottom search-flow strip and subtle local backgrounds. White profile cards with restrained warm-gray borders. Gentle neutral shadows; green accents, no blue glow.
- Typography: Noto Sans for Latin, Noto Sans KR for Korean, sober modern sans-serif. Bold section titles, medium body text. Render Korean text accurately and clearly. Preserve complete footer text.
- All button-like labels, title plates and badges now use small rounded rectangular corners (approximately 6px), replacing long pill shapes. Keep 3D physical objects naturally rounded. No actual new action buttons: the cancellation token light gray and deletion token tomato #FF6347 are reserved UI tokens; there are NO cancel/delete controls in this infographic, so do not add them or introduce arbitrary red decorations.
Content must remain EXACTLY as in input:
"5인 팀 PoC · 개인 기여"
"ZeniManager"
"상담 업무와 유사 사례 검색을 연결하다"
"상담사 대시보드"
"현황 · 점수 · 일정 · 메모"
"실제 DB 연동과 집계 정합성"
"유사 취업사례 검색"
"pgvector 검색 + 조건 재정렬"
"연령대 · 학력 · 전공 반영"
"Electron 세션 안정화"
"401 · 무한 로딩 대응"
"세션 재검증 · 요청 timeout"
"유사 사례를 찾는 과정"
"내담자 정보" / "임베딩"
"벡터 검색" / "pgvector"
"조건 재정렬" / "동일 연령대 우선"
"추천 근거" / "적합도 · 일치 사유"
"React · TypeScript · Electron · Supabase"
"개인 구현 범위 요약 · 운영 성능과 검색 정확도는 별도 검증 필요"
Keep existing small step numbers 1,2,3,4. Keep Electron wording on laptop screen. No added text, no design token swatches, no watermark, no invented claims. Generous whitespace. White opaque background.
```

## 최초 생성

- 도구: 기본 제공 image_gen
- 결과: `../contribution-infographic.png`
- 참고: 사용자가 제공한 actor-critic.png의 입체 일러스트 스타일. 최종 색상은 위 디자인 토큰으로 수정.
- 아래 프롬프트로 생성한 후 한글 문구와 흐름을 육안 확인했습니다.

```text
Use case: infographic-diagram.
Create a polished Korean software engineer portfolio infographic for ZeniManager's GitHub README, landscape 1536x1024 or similar 3:2 proportions, high resolution.
The supplied image is STYLE REFERENCE ONLY: match its white background, deep navy Korean typography, soft blue and turquoise 3D clay illustrations, rounded translucent panels, generous whitespace, dimensional icons, restrained shadows and polished editorial presentation. Create a completely new composition about ZeniManager. Do not reproduce Actor/Critic, scores, feedback loops or user decision buttons from the reference.
Content: personal contributions to a five-person employment counseling management PoC. Three contribution areas: counselor dashboard, similar employment success case search using pgvector, Electron session stability.
Layout: large navy headline at top, smaller subtitle. Across the middle, three generously spaced illustrated zones connected by subtle pale-blue visual continuity, not a table. Left: friendly 3D counselor at a desktop screen showing dashboard charts, calendar and memo. Center: three-dimensional profile documents, magnifying glass and database cylinder connected by blue/turquoise arrows, depicting embedding -> vector search -> rerank -> explanation. Right: laptop with shield, key and circular reconnect arrow depicting session recovery; make this icon professional and not imply certification or perfect security. Beneath each zone a short clear section title and two lines of supporting text. At bottom a distinct light blue horizontal flow strip for the search pipeline, four illustrated steps with slim rightward arrows. Tiny subdued footer states scope. Visual storytelling should dominate, with dimensional illustrations comparable to reference, no flat spreadsheet/card matrix.
Render the following Korean and technical text accurately, no extra invented labels, no performance numbers:
Top headline: "ZeniManager"
Subtitle: "상담 업무와 유사 사례 검색을 연결하다"
Small top context: "5인 팀 PoC · 개인 기여"
Left section title: "상담사 대시보드"
Left supporting lines: "현황 · 점수 · 일정 · 메모" and "실제 DB 연동과 집계 정합성"
Center section title: "유사 취업사례 검색"
Center supporting lines: "pgvector 검색 + 조건 재정렬" and "연령대 · 학력 · 전공 반영"
Right section title: "Electron 세션 안정화"
Right supporting lines: "401 · 무한 로딩 대응" and "세션 재검증 · 요청 timeout"
Bottom strip heading: "유사 사례를 찾는 과정"
Step 1: "내담자 정보" with small caption "임베딩"
Step 2: "벡터 검색" with small caption "pgvector"
Step 3: "조건 재정렬" with small caption "동일 연령대 우선"
Step 4: "추천 근거" with small caption "적합도 · 일치 사유"
Footer: "React · TypeScript · Electron · Supabase"
Additional fine-print footer: "개인 구현 범위 요약 · 운영 성능과 검색 정확도는 별도 검증 필요"
Constraints: beautifully readable Korean, no clipped text, coherent arrows only for actual one-way search process, no circular workflow suggesting dashboard feeds authentication; no invented metrics, no graphs implying measured improvement, no real people's names or personal data, no SVG-style flat geometric substitute. White opaque background.
```
