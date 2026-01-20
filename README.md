# 가상 풍력발전기 기반 지능형 운영 지원 솔루션 개발

![WindTwin](https://img.shields.io/badge/Project-WindTwin-00b4d8?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Active-06d6a0?style=for-the-badge)
![License](https://img.shields.io/badge/License-Proprietary-ff9f1c?style=for-the-badge)

신재생에너지 핵심기술개발사업의 과제 홍보를 위한 웹사이트입니다.

## 📋 목차

- [프로젝트 소개](#프로젝트-소개)
- [주요 기능](#주요-기능)
- [기술 스택](#기술-스택)
- [프로젝트 구조](#프로젝트-구조)
- [설치 및 실행](#설치-및-실행)
- [배포 가이드](#배포-가이드)
- [브라우저 지원](#브라우저-지원)
- [성능 최적화](#성능-최적화)
- [접근성](#접근성)
- [기여](#기여)
- [라이선스](#라이선스)
- [문의](#문의)

## 🌟 프로젝트 소개

**과제명**: 가상 풍력발전기 기반 지능형 운영 지원 솔루션 개발  
**사업명**: 신재생에너지 핵심기술개발사업  
**주관기관**: 디엑스랩즈(주)  
**연구 기간**: 2025년 7월 ~ 2030년 6월 (5년)

### 핵심 목표

고충실도 디지털 트윈과 AI 기술을 결합하여 국내 공통 적용이 가능한 풍력발전기 지능형 운영 및 유지보수 의사결정 지원 솔루션을 개발합니다. 최종 목표는 풍력 발전단지의 운영 및 유지보수(O&M) 비용을 **10% 이상 절감**하는 것입니다.

### 주요 특징

- ✅ **고충실도 디지털 트윈**: 물리 법칙 기반 정밀 시뮬레이션
- ✅ **Living Model**: 실시간 데이터로 자동 최신화
- ✅ **AI 기반 예지보전**: 생성형 AI 활용 고장 예측 (정확도 89%)
- ✅ **OpenFAST 기반**: 다양한 터빈 기종 호환
- ✅ **국내 공통 적용**: 특정 제조사 종속 없는 범용 플랫폼

## 🎯 주요 기능

### 현재 구현된 기능

1. **홈페이지 구조**
   - ✅ 반응형 네비게이션 메뉴
   - ✅ 히어로 섹션 (주요 KPI 애니메이션)
   - ✅ 과제 소개 섹션 (문제-해결-가치 구조)
   - ✅ 핵심 기술 및 차별성 섹션
   - ✅ 추진 체계 (10개 참여기관)
   - ✅ 추진 일정 (5개년 타임라인)
   - ✅ 실증 계획 (5개 실증단지)
   - ✅ 기대 효과 및 주요 지표
   - ✅ FAQ 아코디언
   - ✅ 문의 폼
   - ✅ 푸터

2. **인터랙션**
   - ✅ 스크롤 애니메이션 (AOS)
   - ✅ 숫자 카운터 애니메이션
   - ✅ FAQ 아코디언
   - ✅ 모바일 메뉴 토글
   - ✅ Scroll to Top 버튼
   - ✅ 부드러운 스크롤 네비게이션

3. **디자인**
   - ✅ 모던하고 세련된 UI/UX
   - ✅ 풍력에너지 테마 색상 (청록, 초록)
   - ✅ 반응형 디자인 (모바일/태블릿/데스크톱)
   - ✅ 그라디언트 및 그림자 효과
   - ✅ 마이크로 인터랙션

4. **SEO 및 접근성**
   - ✅ 의미론적 HTML5 태그
   - ✅ Open Graph 메타태그
   - ✅ Twitter Card 메타태그
   - ✅ ARIA 레이블 및 역할
   - ✅ 키보드 네비게이션 지원
   - ✅ 스크린 리더 친화적

## 🛠 기술 스택

### Frontend
- **HTML5**: 의미론적 마크업
- **CSS3**: 
  - CSS Variables (Design Tokens)
  - Flexbox & Grid Layout
  - CSS Animations
  - Media Queries (반응형)
- **JavaScript (ES6+)**:
  - Vanilla JS (No Framework)
  - IntersectionObserver API
  - Fetch API (Form Submission)
  - Event Delegation

### 외부 라이브러리
- **AOS (Animate On Scroll)**: 스크롤 애니메이션
- **Font Awesome 6**: 아이콘
- **Google Fonts**: Noto Sans KR, Roboto

### 도구
- Git (버전 관리)
- Modern Browser DevTools

## 📁 프로젝트 구조

```
windtwin-website/
├── index.html              # 메인 HTML 파일
├── css/
│   └── style.css          # 메인 스타일시트
├── js/
│   └── main.js            # 메인 JavaScript
├── images/                # 이미지 폴더 (선택사항)
│   ├── favicon.png
│   └── og-image.jpg
├── README.md              # 프로젝트 문서
└── .gitignore            # Git 무시 파일
```

## 🚀 설치 및 실행

### 로컬 개발 환경

1. **저장소 클론**
   ```bash
   git clone <repository-url>
   cd windtwin-website
   ```

2. **로컬 서버 실행**
   
   **방법 1: Python 내장 서버**
   ```bash
   # Python 3.x
   python -m http.server 8000
   
   # Python 2.x
   python -m SimpleHTTPServer 8000
   ```
   
   **방법 2: Node.js http-server**
   ```bash
   npx http-server -p 8000
   ```
   
   **방법 3: VS Code Live Server**
   - VS Code에서 `index.html` 우클릭
   - "Open with Live Server" 선택

3. **브라우저에서 확인**
   ```
   http://localhost:8000
   ```

## 🌐 배포 가이드

### 1. GitHub Pages

**단계별 배포:**

1. GitHub 저장소 생성
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin <your-repo-url>
   git push -u origin main
   ```

2. GitHub Pages 활성화
   - GitHub 저장소 → Settings → Pages
   - Source: "Deploy from a branch"
   - Branch: `main` / `(root)` 선택
   - Save

3. 배포 완료
   - 배포 URL: `https://<username>.github.io/<repository-name>/`
   - 약 1-2분 후 접속 가능

**커스텀 도메인 설정 (선택사항):**
```
Settings → Pages → Custom domain
→ 도메인 입력 (예: windtwin.example.com)
→ DNS 설정 (CNAME 레코드)
```

### 2. Netlify

**방법 1: Git 연동 (권장)**

1. [Netlify](https://www.netlify.com/) 로그인
2. "New site from Git" 클릭
3. GitHub 저장소 연결
4. 빌드 설정:
   - Build command: (비워두기)
   - Publish directory: `/`
5. "Deploy site" 클릭

**방법 2: 드래그 앤 드롭**

1. Netlify 대시보드
2. "Sites" → 프로젝트 폴더를 드래그 앤 드롭
3. 자동 배포 완료

**커스텀 도메인:**
```
Site settings → Domain management → Add custom domain
```

**HTTPS 자동 설정:**
- Let's Encrypt SSL 인증서 자동 발급

### 3. Vercel

**CLI 배포:**

1. Vercel CLI 설치
   ```bash
   npm install -g vercel
   ```

2. 로그인 및 배포
   ```bash
   vercel login
   vercel
   ```

3. 프로덕션 배포
   ```bash
   vercel --prod
   ```

**Git 연동:**

1. [Vercel](https://vercel.com/) 로그인
2. "New Project" 클릭
3. GitHub 저장소 Import
4. 자동 배포

### 4. Firebase Hosting

1. Firebase CLI 설치
   ```bash
   npm install -g firebase-tools
   ```

2. 로그인
   ```bash
   firebase login
   ```

3. 프로젝트 초기화
   ```bash
   firebase init hosting
   ```
   - Public directory: `.` (현재 디렉토리)
   - Single-page app: No

4. 배포
   ```bash
   firebase deploy
   ```

### 5. Cloudflare Pages

1. [Cloudflare Pages](https://pages.cloudflare.com/) 로그인
2. "Create a project" 클릭
3. GitHub 저장소 연결
4. 빌드 설정:
   - Build command: (비워두기)
   - Build output directory: `/`
5. "Save and Deploy"

## 🌍 브라우저 지원

| 브라우저 | 버전 |
|---------|------|
| Chrome | 최신 2개 버전 |
| Firefox | 최신 2개 버전 |
| Safari | 최신 2개 버전 |
| Edge | 최신 2개 버전 |
| Mobile Safari (iOS) | 13+ |
| Chrome (Android) | 최신 |

### 폴리필 (선택사항)

ES6+ 기능을 위한 폴리필이 필요한 경우:
```html
<script src="https://cdn.jsdelivr.net/npm/@babel/polyfill@7/dist/polyfill.min.js"></script>
```

## ⚡ 성능 최적화

### 현재 최적화

- ✅ CSS/JS 최소화
- ✅ 이미지 최적화 (WebP 지원)
- ✅ Lazy Loading (이미지)
- ✅ 비동기 스크립트 로딩
- ✅ CDN 사용 (Font Awesome, AOS, Google Fonts)
- ✅ 스크롤 이벤트 쓰로틀링
- ✅ IntersectionObserver 활용

### 추가 최적화 권장사항

1. **이미지 최적화**
   ```bash
   # ImageOptim, TinyPNG 등 사용
   # WebP 포맷 사용 권장
   ```

2. **CSS/JS 압축**
   ```bash
   # UglifyJS, Terser, cssnano 등
   npm install -g terser cssnano
   terser js/main.js -o js/main.min.js
   ```

3. **CDN 캐싱**
   - Cloudflare, Fastly 등 CDN 활용
   - 적절한 Cache-Control 헤더 설정

4. **리소스 힌트**
   ```html
   <link rel="preconnect" href="https://fonts.googleapis.com">
   <link rel="dns-prefetch" href="https://cdn.jsdelivr.net">
   ```

## ♿ 접근성

### WCAG 2.1 AA 준수

- ✅ 적절한 색상 대비율 (4.5:1 이상)
- ✅ 키보드 네비게이션 지원
- ✅ ARIA 레이블 및 역할
- ✅ 의미론적 HTML
- ✅ 포커스 표시자
- ✅ 스크린 리더 지원

### 테스트 도구

- **WAVE**: 웹 접근성 평가 도구
- **axe DevTools**: Chrome 확장 프로그램
- **Lighthouse**: Chrome DevTools

## 📊 SEO 최적화

### 체크리스트

- ✅ 의미론적 HTML5 태그
- ✅ 메타 태그 (title, description)
- ✅ Open Graph 태그
- ✅ Twitter Card 태그
- ✅ 구조화된 데이터 (Schema.org) - 추가 권장
- ✅ Sitemap.xml - 추가 권장
- ✅ Robots.txt - 추가 권장
- ✅ 모바일 친화적
- ✅ 빠른 로딩 속도

### 추가 권장 파일

**sitemap.xml** (루트 디렉토리):
```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  <url>
    <loc>https://your-domain.com/</loc>
    <lastmod>2025-01-20</lastmod>
    <changefreq>monthly</changefreq>
    <priority>1.0</priority>
  </url>
</urlset>
```

**robots.txt** (루트 디렉토리):
```
User-agent: *
Allow: /
Sitemap: https://your-domain.com/sitemap.xml
```

## 🎨 디자인 토큰

### 색상 팔레트

```css
/* Primary (Wind Energy Blue) */
--color-primary: #00b4d8
--color-primary-dark: #0096c7
--color-primary-light: #48cae4

/* Secondary (Energy Green) */
--color-secondary: #06d6a0
--color-secondary-dark: #05b886

/* Accent (Innovation Orange) */
--color-accent: #ff9f1c
```

### 타이포그래피

- **한글**: Noto Sans KR (300, 400, 500, 600, 700, 900)
- **영문**: Roboto (300, 400, 500, 700, 900)

## 🐛 알려진 이슈

현재 알려진 이슈가 없습니다.

## 🔜 향후 계획

- [ ] 다국어 지원 (영문)
- [ ] 관리자 페이지 (과제 진행 상황 업데이트)
- [ ] 블로그/뉴스 섹션
- [ ] 갤러리 (실증 사진/동영상)
- [ ] 다운로드 센터 (백서, 보고서)
- [ ] 검색 기능
- [ ] 다크 모드

## 🤝 기여

본 프로젝트는 디엑스랩즈(주)가 관리하는 proprietary 프로젝트입니다.

## 📄 라이선스

Copyright © 2025 디엑스랩즈(주). All rights reserved.

본 프로젝트는 신재생에너지 핵심기술개발사업의 일환으로 개발되었습니다.

## 📞 문의

**주관기관**: 디엑스랩즈(주)  
**이메일**: contact@dxlabs.co.kr  
**전화**: 02-XXXX-XXXX  
**운영 시간**: 평일 09:00 - 18:00

---

## 📌 체크리스트 (배포 전 확인)

### 콘텐츠
- [ ] 모든 텍스트 내용 검토 완료
- [ ] 연락처 정보 업데이트
- [ ] 이미지 파일 준비 (favicon, og-image)
- [ ] 실증단지 지도 이미지/인터랙티브 맵

### 기술
- [ ] 모든 브라우저에서 테스트
- [ ] 모바일 기기에서 테스트
- [ ] 접근성 테스트 (WAVE, axe)
- [ ] Lighthouse 점수 확인
- [ ] 404 페이지 생성
- [ ] Sitemap.xml 추가
- [ ] Robots.txt 추가

### SEO
- [ ] Google Search Console 등록
- [ ] Google Analytics 설정
- [ ] Open Graph 이미지 생성
- [ ] 메타 태그 최적화

### 보안
- [ ] HTTPS 설정
- [ ] CSP (Content Security Policy) 헤더
- [ ] CORS 설정 확인

---

**Last Updated**: 2025-01-20  
**Version**: 1.0.0  
**Author**: 디엑스랩즈(주)