# 배포 가이드 (DEPLOYMENT.md)

이 문서는 WindTwin 웹사이트를 실제 서버에 배포하는 상세 가이드입니다.

## 📋 목차

1. [배포 전 준비사항](#배포-전-준비사항)
2. [GitHub Pages 배포](#1-github-pages-배포)
3. [Netlify 배포](#2-netlify-배포)
4. [Vercel 배포](#3-vercel-배포)
5. [커스텀 도메인 설정](#커스텀-도메인-설정)
6. [배포 후 확인사항](#배포-후-확인사항)

---

## 배포 전 준비사항

### 1. 파일 확인

```
✅ index.html
✅ css/style.css
✅ js/main.js
✅ README.md
⚠️ images/favicon.png (선택사항)
⚠️ images/og-image.jpg (선택사항)
```

### 2. 내용 업데이트

**index.html에서 다음 항목을 업데이트하세요:**

1. **연락처 정보** (Line 558-578)
   ```html
   <p><a href="mailto:contact@dxlabs.co.kr">contact@dxlabs.co.kr</a></p>
   <p>02-XXXX-XXXX</p>
   ```

2. **Open Graph URL** (Line 16)
   ```html
   <meta property="og:url" content="https://your-domain.com">
   ```

3. **Open Graph Image** (Line 15)
   ```html
   <meta property="og:image" content="https://your-domain.com/images/og-image.jpg">
   ```

### 3. 이미지 준비

**필수 이미지:**

1. **Favicon** (`images/favicon.png`)
   - 크기: 512x512px
   - 포맷: PNG
   - 용도: 브라우저 탭 아이콘

2. **Open Graph Image** (`images/og-image.jpg`)
   - 크기: 1200x630px
   - 포맷: JPG
   - 용도: 소셜 미디어 공유 시 미리보기

**이미지가 없는 경우:**
- Favicon: https://via.placeholder.com/512
- OG Image: https://via.placeholder.com/1200x630

---

## 1. GitHub Pages 배포

### 방법 A: 웹 인터페이스 (초보자 추천)

1. **GitHub 계정 생성**
   - https://github.com 접속
   - 계정 생성 (무료)

2. **새 저장소 생성**
   - 우측 상단 "+" → "New repository"
   - Repository name: `windtwin-website` (또는 원하는 이름)
   - Public 선택
   - "Create repository" 클릭

3. **파일 업로드**
   - "uploading an existing file" 클릭
   - 모든 파일을 드래그 앤 드롭
   - Commit message: "Initial commit"
   - "Commit changes" 클릭

4. **GitHub Pages 활성화**
   - 저장소 → "Settings" 탭
   - 좌측 메뉴 → "Pages"
   - Source: "Deploy from a branch"
   - Branch: `main` 선택, Folder: `/ (root)` 선택
   - "Save" 클릭

5. **배포 완료**
   - 1-2분 후 페이지 상단에 URL 표시
   - 예: `https://username.github.io/windtwin-website/`

### 방법 B: Git CLI (개발자 추천)

```bash
# 1. Git 설치 확인
git --version

# 2. 프로젝트 폴더에서 Git 초기화
cd windtwin-website
git init

# 3. 파일 추가 및 커밋
git add .
git commit -m "Initial commit: WindTwin website"

# 4. GitHub 저장소와 연결
git remote add origin https://github.com/YOUR_USERNAME/windtwin-website.git

# 5. 푸시
git branch -M main
git push -u origin main

# 6. GitHub 웹사이트에서 Pages 활성화 (위 방법 A의 4번 참조)
```

### 업데이트 방법

```bash
# 파일 수정 후
git add .
git commit -m "Update: [변경 내용 설명]"
git push
# 자동으로 재배포됨 (1-2분 소요)
```

---

## 2. Netlify 배포

### 방법 A: 드래그 앤 드롭 (가장 간단)

1. **Netlify 가입**
   - https://www.netlify.com 접속
   - "Sign up" (GitHub 계정 연동 권장)

2. **배포**
   - 로그인 후 대시보드
   - 프로젝트 폴더를 화면에 드래그 앤 드롭
   - 자동 배포 시작

3. **완료**
   - 배포 완료 시 URL 자동 생성
   - 예: `https://random-name-123456.netlify.app`

### 방법 B: GitHub 연동 (권장)

1. **Netlify 로그인**
   - GitHub 계정으로 로그인

2. **새 사이트 생성**
   - "New site from Git" 클릭
   - "GitHub" 선택
   - 저장소 선택 (windtwin-website)

3. **빌드 설정**
   ```
   Build command: (비워두기)
   Publish directory: /
   ```

4. **배포**
   - "Deploy site" 클릭
   - 자동 배포 시작

### 자동 배포

GitHub와 연동 시, `git push` 할 때마다 자동으로 재배포됩니다.

### 사이트 이름 변경

1. Site settings → Site details
2. "Change site name" 클릭
3. 원하는 이름 입력 (예: windtwin-project)
4. URL: `https://windtwin-project.netlify.app`

---

## 3. Vercel 배포

### 방법 A: 웹 인터페이스

1. **Vercel 가입**
   - https://vercel.com 접속
   - GitHub 계정으로 로그인

2. **Import Project**
   - "New Project" 클릭
   - "Import Git Repository"
   - GitHub 저장소 선택

3. **설정**
   ```
   Framework Preset: Other
   Build Command: (비워두기)
   Output Directory: ./
   ```

4. **배포**
   - "Deploy" 클릭
   - URL 자동 생성: `https://windtwin-website.vercel.app`

### 방법 B: CLI

```bash
# 1. Vercel CLI 설치
npm install -g vercel

# 2. 로그인
vercel login

# 3. 프로젝트 폴더에서 배포
cd windtwin-website
vercel

# 4. 프로덕션 배포
vercel --prod
```

---

## 커스텀 도메인 설정

### Netlify에서 커스텀 도메인 연결

1. **도메인 구입**
   - 예: windtwin.co.kr (가비아, 호스팅케이알 등)

2. **Netlify 설정**
   - Site settings → Domain management
   - "Add custom domain" 클릭
   - 도메인 입력: `windtwin.co.kr`

3. **DNS 설정**
   - 도메인 등록 업체 사이트 접속
   - DNS 관리 페이지
   - 다음 레코드 추가:
   
   ```
   Type: CNAME
   Name: www
   Value: your-site.netlify.app
   
   Type: A
   Name: @
   Value: 75.2.60.5 (Netlify IP)
   ```

4. **SSL 인증서**
   - Netlify에서 자동으로 Let's Encrypt SSL 발급
   - HTTPS 자동 적용

### GitHub Pages에서 커스텀 도메인

1. **저장소 루트에 `CNAME` 파일 생성**
   ```
   windtwin.co.kr
   ```

2. **DNS 설정**
   ```
   Type: CNAME
   Name: www
   Value: username.github.io
   
   Type: A (4개 모두 추가)
   Name: @
   Value: 185.199.108.153
   Value: 185.199.109.153
   Value: 185.199.110.153
   Value: 185.199.111.153
   ```

3. **GitHub Pages 설정**
   - Settings → Pages
   - Custom domain에 도메인 입력
   - "Enforce HTTPS" 체크

---

## 배포 후 확인사항

### ✅ 체크리스트

1. **기능 테스트**
   - [ ] 모든 링크 작동 확인
   - [ ] 네비게이션 메뉴 작동
   - [ ] 문의 폼 제출 테스트
   - [ ] FAQ 아코디언 작동
   - [ ] 모바일 메뉴 토글

2. **브라우저 호환성**
   - [ ] Chrome
   - [ ] Firefox
   - [ ] Safari
   - [ ] Edge
   - [ ] Mobile Safari (iOS)
   - [ ] Chrome Mobile (Android)

3. **반응형 테스트**
   - [ ] 데스크톱 (1920px)
   - [ ] 노트북 (1366px)
   - [ ] 태블릿 (768px)
   - [ ] 모바일 (375px)

4. **성능 테스트**
   ```
   Chrome DevTools → Lighthouse
   
   목표:
   - Performance: 90+
   - Accessibility: 90+
   - Best Practices: 90+
   - SEO: 90+
   ```

5. **SEO 확인**
   - [ ] Google Search Console 등록
   - [ ] Sitemap 제출
   - [ ] Robots.txt 확인
   - [ ] Open Graph 미리보기 (Facebook Debugger)
   - [ ] Twitter Card 미리보기

### 🔧 문제 해결

**CSS/JS가 로드되지 않는 경우:**
```html
<!-- 절대 경로 대신 상대 경로 사용 -->
<link rel="stylesheet" href="./css/style.css">
<script src="./js/main.js"></script>
```

**이미지가 표시되지 않는 경우:**
```html
<!-- 경로 확인 -->
<img src="./images/logo.png" alt="Logo">
```

**GitHub Pages에서 404 오류:**
- 저장소가 Public인지 확인
- Pages가 활성화되었는지 확인
- 브랜치와 폴더 설정 확인

---

## 📊 모니터링 및 분석

### Google Analytics 추가

1. **Google Analytics 계정 생성**
   - https://analytics.google.com

2. **추적 코드 추가**
   ```html
   <!-- index.html의 </head> 전에 추가 -->
   <!-- Google tag (gtag.js) -->
   <script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
   <script>
     window.dataLayer = window.dataLayer || [];
     function gtag(){dataLayer.push(arguments);}
     gtag('js', new Date());
     gtag('config', 'G-XXXXXXXXXX');
   </script>
   ```

### Google Search Console

1. **사이트 등록**
   - https://search.google.com/search-console

2. **소유권 확인**
   - HTML 태그 방법 선택
   - 메타 태그를 `<head>`에 추가

3. **Sitemap 제출**
   - `https://your-domain.com/sitemap.xml`

---

## 🔒 보안 설정

### HTTPS 강제

**Netlify:**
- HTTPS → Automatic (기본 설정)

**GitHub Pages:**
- Settings → Pages → Enforce HTTPS 체크

### 보안 헤더 (Netlify)

`netlify.toml` 파일 생성:
```toml
[[headers]]
  for = "/*"
  [headers.values]
    X-Frame-Options = "DENY"
    X-Content-Type-Options = "nosniff"
    X-XSS-Protection = "1; mode=block"
    Referrer-Policy = "strict-origin-when-cross-origin"
```

---

## 📞 지원

배포 중 문제가 발생하면:

- **GitHub Pages**: https://docs.github.com/pages
- **Netlify**: https://docs.netlify.com
- **Vercel**: https://vercel.com/docs

또는 프로젝트 담당자에게 문의:
- 이메일: contact@dxlabs.co.kr

---

**마지막 업데이트**: 2025-01-20  
**버전**: 1.0.0