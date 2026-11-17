# 채온에스테틱 홈페이지

정적 사이트(빌드 없음) · Cloudflare Pages 배포 · 관리자(편집 모드) 포함.

## 배포
- Cloudflare Pages: Framework preset None / Build command 비움 / Build output directory `/`
- 도메인을 연결하면 sitemap.xml, robots.txt, rss.xml, 각 html 의 canonical·og:url 주소를 그 도메인으로 맞춥니다(현재 chaeonaesthetic.pages.dev).

## 관리자(편집 모드)
- 주소: /edit (비밀번호 로그인). 글자는 눌러서 고치고, 사진은 눌러서 바꾼 뒤 "저장하기".
- 저장하면 content/text.json(문구), content/media.json(사진), assets/uploads/(새 사진)에 기록되고 1분 안쪽으로 홈페이지에 반영됩니다.
- Cloudflare Pages 환경 변수: GITHUB_TOKEN(이 저장소 Contents 읽기·쓰기), CMS_PASSWORD(편집 비밀번호).

## 구조
- index.html, brand.html, program.html, cases.html, review.html, contact.html: 페이지(원래 한 파일 번들을 풀어 놓은 것)
- assets/b/: 페이지 구성 요소·글꼴·공용 사진(내용 해시 이름, 1년 캐시)
- assets/photos/: 사진, assets/chaeon-m.css: 모바일 손질, assets/sj-cms.js·sj-editor.js: 관리자
