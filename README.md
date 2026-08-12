# 1Irving1의 기술 블로그

https://1irving1.github.io — Jekyll + [Chirpy](https://github.com/cotes2020/jekyll-theme-chirpy) 테마, GitHub Pages(Actions) 배포.

## 글쓰기

**https://1irving1.github.io/admin** 접속 → GitHub 계정으로 로그인 → New Post.

- 이 페이지는 관리자 전용 글쓰기 도구이며, 방문자가 보는 실제 블로그(루트 주소)와는 별개 화면임
- 여기서 글을 저장하면 `_posts`에 자동 커밋되고, 몇 분 안에 실제 블로그에 반영됨
- 항목: Title(제목), Publish Date(발행일), Categories(분류, 여러 개 가능), Tags(태그), Thumbnail(썸네일, 선택), Body(본문, 마크다운)
- Thumbnail을 넣으면 홈 화면 글 목록 카드에 큰 썸네일 이미지로 나타남 (Chirpy 기본 기능, `image:` 프론트매터). 안 넣으면 지금처럼 텍스트만 나오는 카드로 자연스럽게 나옴

### 안 될 때

`github.com`이 아니라 `netlify.com`으로 리다이렉트되면 로그인 프록시(Cloudflare Worker) 문제.
- Worker: `decap-oauth-1irving1.decap-oauth-worker.workers.dev` (로컬 소스: `~/decap-oauth-worker`)
- GitHub OAuth App: https://github.com/settings/developers → `1Irving1 Blog CMS`

관리자 도구 없이도 `_posts` 폴더에서 GitHub 웹 UI로 직접 마크다운 파일을 만들어도 됨 (설정 불필요, 항상 되는 방법).

## 로컬 구조

- `_config.yml` — 사이트 설정 (제목, 소셜 링크, 다크모드, PWA 등)
- `assets/` — 이미지 등 정적 파일
- `admin/` — 글쓰기 도구(Decap CMS) 설정
