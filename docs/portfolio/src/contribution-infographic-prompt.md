# ZeniManager 포트폴리오 인포그래픽 제작 기록

- 도구: 기본 제공 image_gen
- 결과: `../contribution-infographic.png`
- 참고: 사용자가 제공한 actor-critic.png의 입체 일러스트와 색상 스타일
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
