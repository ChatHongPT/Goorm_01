# Goorm Neflix Clone 🎬

[![MIT License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![HTML](https://img.shields.io/badge/HTML-5-orange.svg)](https://developer.mozilla.org/ko/docs/Web/HTML)
[![CSS](https://img.shields.io/badge/CSS-3-blue.svg)](https://developer.mozilla.org/ko/docs/Web/CSS)
[![Netlify](https://img.shields.io/badge/CI/CD-GitHubPages-brightgreen.svg)](https://yourusername.github.io/netflix-clone/)

---

## 📌 프로젝트 개요

이 프로젝트는 **HTML**과 **CSS**로 만든 **넷플릭스 클론**입니다.  

주요 구성:
- 상단 로고 및 프로필 포함 내비게이션 바
- 재생/저장 버튼이 있는 메인 배너
- 가로로 스크롤되는 영화 카드 리스트

---

## 💿 CI/CD Workflow

이 프로젝트는 **GitHub Actions**로 자동 배포됩니다.  
`main` 브랜치에 푸시할 때마다 `.github/workflows/deploy.yml` 파일이 실행되어  
`gh-pages` 브랜치로 코드가 배포되고, GitHub Pages에서 웹사이트로 서비스됩니다.

✅ 배포 주소: [https://chathongpt.github.io/Groom_01/](https://chathongpt.github.io/Groom_01/)

```bash
name: Deploy static HTML to GitHub Pages

on:
  push:
    branches:
      - main

permissions:
  contents: write # gh-pages 브랜치로 푸시할 수 있도록 권한 부여

jobs:
  deploy:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout source
        uses: actions/checkout@v3

      - name: Deploy to GitHub Pages
        uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: . # index.html, style.css가 있는 위치
          publish_branch: gh-pages

```
---

## 📂 주요 기능

✅ 반응형 디자인  
✅ 카드 hover 효과  
✅ 깔끔한 섹션 분리  
✅ GitHub Actions를 통한 자동 배포

---

## 🛠 사용 기술

- **HTML5**
- **CSS3**
- **GitHub Pages + GitHub Actions**

---

## 💡 배포 워크플로 상세

- `main` 브랜치에 커밋 → GitHub Actions가 실행됨
- `gh-pages` 브랜치로 자동 푸시 → GitHub Pages에서 최신 버전 제공

---

## 📸 스크린샷

| 메인 배너  | 
| ---------- |
| ![banner](https://github.com/user-attachments/assets/d79d97df-0c85-4a4d-9085-4aab197849c1) |

## 🚀 실행 방법

1️⃣ 레포지토리 클론:
```bash
git clone https://github.com/yourusername/netflix-clone.git
```

---
