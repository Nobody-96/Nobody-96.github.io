# Jincheol Yang — Academic Homepage

GitHub Pages용 개인 홈페이지입니다. 빌드 과정 없이 `index.html` 하나로 동작합니다.

```
index.html                  ← 페이지 전체 (디자인 + 내용)
assets/profile.jpg          ← 프로필 사진
assets/Jincheol_Yang_CV.pdf ← CV 버튼에 연결된 파일
```

## 배포하기 (5분)

1. GitHub에 로그인한 뒤 **New repository**를 누릅니다.
2. Repository 이름을 반드시 `<내 GitHub 아이디>.github.io` 로 정하고, **Public**으로 만듭니다.
   예: 아이디가 `jincheol-yang`이면 `jincheol-yang.github.io`
3. 만들어진 저장소 화면에서 **Add file → Upload files**를 누르고, 이 폴더 안의 `index.html`, `README.md`, `assets` 폴더를 통째로 끌어다 놓은 뒤 **Commit changes**를 누릅니다.
4. **Settings → Pages**에서 Source가 `Deploy from a branch`, Branch가 `main` / `(root)`인지 확인합니다.
5. 1~2분 뒤 `https://<내 GitHub 아이디>.github.io` 로 접속하면 완성입니다.

## 내용 수정하기

저장소에서 `index.html`을 열고 연필 아이콘(Edit)을 눌러 바로 고칠 수 있습니다.

**논문 추가:** 파일 아래쪽 `const PUBS = [` 배열에서 항목 하나를 복사해 맨 위에 붙여넣고 내용만 바꾸면 됩니다. 개수, 필터, 1저자 표시는 자동으로 계산됩니다.

```js
{ type: "conference", venue: "CVPR 2027",
  title: "논문 제목",
  authors: "Jincheol Yang, Coauthor A, Suk-Ju Kang†",
  links: { Paper: "https://...", Code: "https://github.com/..." } },
```

- `type`: `conference` / `workshop` / `journal` / `review`(심사 중)
- 심사 중이던 논문이 붙으면 `type`과 `venue`만 바꿔 주세요.
- `links`에는 `Paper`, `Code`, `Project` 등 원하는 이름으로 여러 개 넣을 수 있습니다.

**사진 교체:** `assets/profile.jpg`를 같은 이름으로 덮어쓰면 됩니다. 세로 4:5 비율이 가장 잘 맞습니다.

**CV 교체:** `assets/Jincheol_Yang_CV.pdf`를 같은 이름으로 덮어쓰면 됩니다.

**경력·수상·서비스:** `index.html` 본문의 `Research experience`, `Awards`, `Academic service` 부분에서 `<li class="tl">…</li>` 블록을 복사해 추가하세요. 진행 중인 항목은 날짜에 `class="when now"`를 쓰면 빨간 점이 붙습니다.

## 참고

- 다크 모드는 방문자의 시스템 설정을 자동으로 따릅니다.
- 상단의 계단 모양 그래프는 양자화(quantization)를 표현한 것으로, 클릭하면 비트 수가 2 → 3 → 4 → 6 → 8로 바뀝니다.
- 카카오톡·슬랙 등에 링크를 공유할 때 미리보기 사진이 나오게 하려면, `index.html` 상단의 `og:image` 값을 `https://<아이디>.github.io/assets/profile.jpg` 처럼 전체 주소로 바꿔 주세요.
- 하단의 "Last updated" 날짜는 배포할 때마다 자동으로 갱신됩니다.
