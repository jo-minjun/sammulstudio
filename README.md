# 샘물스튜디오

sammulstudio.com에 GitHub Pages로 게시하는 샘물스튜디오 웹사이트다. main 브랜치의 루트를 게시한다. 빌드 도구 없이 정적 HTML을 이 저장소에서 직접 고친다.

## 구조

| 경로 | 내용 |
|---|---|
| `index.html` | 스튜디오 첫 페이지 |
| `honey-bloom/ko/`, `honey-bloom/en/` | Honey Bloom 소개 페이지 |
| `honey-bloom/privacy/ko/`, `honey-bloom/privacy/en/` | Honey Bloom 개인정보처리방침 |
| `honey-bloom/terms/ko/`, `honey-bloom/terms/en/` | Honey Bloom 이용약관 |
| `honey-bloom/support/ko/`, `honey-bloom/support/en/` | Honey Bloom 지원 페이지 |
| `assets/site.css`, `assets/lang.js`, `assets/fonts/pretendard/` | Honey Bloom 페이지의 스타일, 언어 이동 스크립트, Pretendard 글꼴 |
| `assets/og-image.png`, `favicon.ico`, `apple-touch-icon.png` | 링크 미리보기 이미지와 아이콘 |
| `app-ads.txt` | AdMob 앱 확인 파일 |
| `sitemap.xml`, `robots.txt` | 검색 엔진용 파일 |

Honey Bloom 페이지와 `assets/`는 2026-11-23에 [jo-minjun/jo-minjun.github.io](https://github.com/jo-minjun/jo-minjun.github.io)의 `docs/`에서 옮겼다. 그 저장소의 `docs/honey-bloom/`에는 이 사이트의 같은 경로로 보내는 넘김 페이지만 남아 있다. 디자인 기준은 그 저장소의 `DESIGN.md`에 있다. 두 저장소의 `site.css`는 따로 관리하므로, 한쪽을 고쳐도 다른 쪽은 바뀌지 않는다.

언어 폴더가 없는 주소(`/honey-bloom/`, `/honey-bloom/privacy/` 등)는 `assets/lang.js`가 `ko/` 또는 `en/`으로 보내는 언어 이동 페이지다. 두 언어 파일은 같은 내용을 담는다. 한쪽을 고치면 다른 쪽도 함께 고친다.

## 주소를 바꾸면 안 되는 파일

아래 주소는 외부 서비스와 앱 코드에 등록되어 있다. 파일을 옮기거나 이름을 바꾸지 않는다.

| 주소 | 등록된 곳 |
|---|---|
| `/honey-bloom/privacy/` | Honey Bloom 앱 설정 화면, App Store Connect, Play Console |
| `/honey-bloom/support/` | App Store Connect |
| `/app-ads.txt` | AdMob. 도메인 최상위 경로에서만 찾는다 |

Honey Bloom이 새 정보를 수집·저장·전송하거나 새 알림·권한을 쓰면 `honey-bloom/privacy/ko/index.html`과 `honey-bloom/privacy/en/index.html`을 함께 고치고, 두 파일의 시행일도 바꾼다.

페이지를 더하거나 지우면 `sitemap.xml`도 함께 고친다.
