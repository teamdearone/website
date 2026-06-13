# Dear One — 회사 소개 웹사이트

아동발달치료센터를 위한 치료 운영 OS, **Dear One**의 공식 소개 사이트입니다.
빌드 과정 없이 바로 배포되는 정적 사이트입니다.

## 구성

- `index.html` — 사이트 전체(홈·제품·팀·베타 파트너 4개 화면을 한 파일에서 전환하는 SPA). HTML/CSS/JS·이미지가 모두 한 파일에 들어 있습니다.
- `DearOne-Brochure-2026.pdf` — 푸터의 "서비스 소개서 (PDF)" 다운로드 링크가 가리키는 소개서.
- `.nojekyll` — GitHub Pages의 Jekyll 처리를 비활성화(정적 파일 그대로 서빙).

## 배포 (GitHub Pages)

1. 이 저장소에 변경 사항을 push 합니다.
2. GitHub 저장소 → **Settings → Pages** 로 이동합니다.
3. **Source** 를 `Deploy from a branch`, **Branch** 를 `main` / `/ (root)` 로 설정하고 저장합니다.
4. 1~2분 뒤 `https://teamdearone.github.io/website/` 에서 사이트가 열립니다.

### 커스텀 도메인 (선택)

`team.dearone.kr` 같은 도메인을 연결하려면:

1. Settings → Pages → **Custom domain** 에 도메인을 입력합니다(저장 시 저장소에 `CNAME` 파일이 생성됨).
2. 도메인 DNS에 GitHub Pages용 레코드(CNAME 또는 A 레코드)를 추가합니다.
3. 연결 후 `index.html` 상단의 주석 처리된 `canonical` / `og:url` / `og:image` 블록을 해제하고 `yourdomain.kr` 을 실제 도메인으로 교체합니다. (카카오톡/SNS 공유 미리보기용 `og-image.png` 를 같은 위치에 업로드)

## 배포 전 꼭 해야 할 것

- [ ] **베타 신청 폼 연동** — `index.html` 의 `WEB3FORMS_KEY` 값이 아직 `YOUR_ACCESS_KEY_HERE` 입니다.
  [web3forms.com](https://web3forms.com) 에서 `team.dearone@gmail.com` 으로 무료 가입 → 발급받은 Access Key 를 그 한 줄에 붙여넣으면, 신청서가 해당 메일로 자동 접수됩니다.
  (키를 넣기 전에는 폼 제출 시 "메일로 보내달라"는 안내 문구가 표시됩니다.)
- [ ] (선택) 위 커스텀 도메인 / OG 이미지 설정.
