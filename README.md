# 샘물스튜디오

sammulstudio.com에 GitHub Pages로 게시하는 샘물스튜디오 웹사이트다. main 브랜치의 루트를 게시한다. 빌드 도구 없이 정적 HTML을 이 저장소에서 직접 고친다.

## 구조

| 경로 | 내용 |
|---|---|
| `index.html` | 언어 이동 페이지. `ko/` 또는 `en/`으로 보낸다 |
| `ko/`, `en/` | 스튜디오 첫 페이지. 스튜디오 이름과 게임 카드 목록 |
| `honey-bloom/ko/`, `honey-bloom/en/` | Honey Bloom 소개 페이지 |
| `honey-bloom/privacy/ko/`, `honey-bloom/privacy/en/` | Honey Bloom 개인정보처리방침 |
| `honey-bloom/terms/ko/`, `honey-bloom/terms/en/` | Honey Bloom 이용약관 |
| `honey-bloom/support/ko/`, `honey-bloom/support/en/` | Honey Bloom 지원 페이지 |
| `assets/site.css`, `assets/lang.js`, `assets/fonts/pretendard/` | 모든 페이지의 스타일, 언어 이동 스크립트, Pretendard 글꼴 |
| `assets/og-image.png`, `favicon.ico`, `apple-touch-icon.png` | 링크 미리보기 이미지와 아이콘 |
| `app-ads.txt` | AdMob 앱 확인 파일 |
| `sitemap.xml`, `robots.txt` | 검색 엔진용 파일 |

Honey Bloom 페이지와 `assets/`는 2026-11-23에 [jo-minjun/jo-minjun.github.io](https://github.com/jo-minjun/jo-minjun.github.io)의 `docs/`에서 옮겼다. 그 저장소의 `docs/honey-bloom/`에는 이 사이트의 같은 경로로 보내는 넘김 페이지만 남아 있다. 디자인 기준은 그 저장소의 `DESIGN.md`에 있다. 두 저장소의 `site.css`는 따로 관리하므로, 한쪽을 고쳐도 다른 쪽은 바뀌지 않는다.

언어 폴더가 없는 주소(`/`, `/honey-bloom/`, `/honey-bloom/privacy/` 등)는 `assets/lang.js`가 `ko/` 또는 `en/`으로 보내는 언어 이동 페이지다. 두 언어 파일은 같은 내용을 담는다. 한쪽을 고치면 다른 쪽도 함께 고친다. 한국어 본문은 `~다`체로 쓰고, 지원 페이지의 자주 묻는 질문 답변만 `~습니다`체로 쓴다.

## 사이트 이름과 이미지

모든 페이지의 사이트 이름은 한국어 페이지에서 "샘물스튜디오", 영어 페이지와 언어 이동 페이지에서 "Sammul Studio"다. 이 이름은 `og:site_name`, `og:image:alt`, 푸터, 첫 페이지 제목에 쓴다. 푸터는 이름(첫 페이지로 가는 링크)과 "모바일 게임 스튜디오"("Mobile game studio")를 담는다.

세 이미지는 `site.css`와 같은 색상(`--ink` #141414, `--faint` #adadad)과 Pretendard로 그렸다. 글자나 값을 바꾸려면 아래 값으로 다시 그린다.

| 파일 | 크기 | 구성 |
|---|---|---|
| `favicon.ico` | 16·32·48px | `--ink` 원 안에 흰색 "샘"을 652 굵기로 쓴다. 글꼴 크기는 아이콘 크기의 약 67%이고, 글자는 잉크 영역 기준으로 원의 가운데에 둔다. 32비트 BMP 항목 3개다. |
| `apple-touch-icon.png` | 180px | 같은 글자를 꽉 찬 `--ink` 정사각형에 쓴다. 글꼴 크기는 아이콘 크기의 약 55%다. iOS가 모서리를 직접 둥글게 자르므로 모서리를 둥글게 하지 않는다. |
| `assets/og-image.png` | 1200×630 | 푸터와 같은 반전 화면이다. `--ink` 배경에 "샘물스튜디오"(184px, 652, 줄 간격 1.15)와 "Sammul Studio"(64px, 300, `--faint`, 위 간격 8px)를 쌓는다. 아래 줄 왼쪽에 "Mobile game studio"(34px, `--faint`), 오른쪽에 "sammulstudio.com"(34px, 600)을 둔다. 안쪽 여백은 위와 좌우 96px, 아래 80px이다. |

## 주소를 바꾸면 안 되는 파일

아래 주소는 외부 서비스와 앱 코드에 등록되어 있다. 파일을 옮기거나 이름을 바꾸지 않는다.

| 주소 | 등록된 곳 |
|---|---|
| `/honey-bloom/privacy/` | Honey Bloom 앱 설정 화면, App Store Connect, Play Console |
| `/honey-bloom/support/` | App Store Connect |
| `/app-ads.txt` | AdMob. 도메인 최상위 경로에서만 찾는다 |

Honey Bloom이 새 정보를 수집·저장·전송하거나 새 알림·권한을 쓰면 `honey-bloom/privacy/ko/index.html`과 `honey-bloom/privacy/en/index.html`을 함께 고치고, 두 파일의 시행일도 바꾼다.

Honey Bloom 문서의 운영자는 "샘물스튜디오(운영자 조민준)"로 쓰고, 개인정보 보호책임자는 조민준으로 쓴다. 계약과 개인정보 처리의 법적 주체를 밝히려고 개인 이름을 함께 쓴다. 샘물스튜디오를 사업자등록하면 상호, 대표자, 사업자등록번호 등 표시 사항을 다시 확인한다.

문의 이메일은 `support@sammulstudio.com`이다. 개인정보처리방침, 이용약관, 지원 페이지(각 한국어·영어)에 있다. 주소를 바꾸면 이 6개 파일, Honey Bloom 앱 코드, App Store Connect와 Play Console의 연락처를 함께 고친다.

페이지를 더하거나 지우면 `sitemap.xml`도 함께 고친다.
