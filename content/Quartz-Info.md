# Quartz 4 프로젝트 정보

## 📋 프로젝트 개요

- **프로젝트 이름**: Quartz 4
- **버전**: 4.5.1
- **라이선스**: MIT
- **개발자**: jackyzha0 (j.zhao2k19@gmail.com)
- **공식 홈페이지**: https://quartz.jzhao.xyz
- **GitHub 저장소**: https://github.com/jackyzha0/quartz.git
- **프로젝트 설명**: 디지털 가든(Digital Garden)과 노트를 웹사이트로 무료 출판할 수 있는 정적 사이트 생성기(Static Site Generator)

## 🎯 핵심 목적

- **디지털 가든 출판**: 개인의 지식 노트와 메모를 웹사이트 형태로 쉽게 공유
- **Obsidian 호환성**: Obsidian 볼트를 그대로 웹사이트로 변환 가능
- **마크다운 기반**: 마크다운 파일을 완전한 기능의 웹사이트로 변환
- **확장성**: 개발자가 플러그인과 컴포넌트를 통해 자유롭게 커스터마이징 가능

## 🛠 기술 스택

### 📦 핵심 런타임 환경
- **Node.js**: 22+ (최소 요구사항)
- **npm**: 10.9.2+ (패키지 관리)
- **TypeScript**: 5.9.2 (정적 타입 체크 언어)

### 🎨 프론트엔드 기술
- **Preact**: 10.27.0 (경량 React 대안, 가상 DOM 라이브러리)
- **JSX**: React-jsx (컴포넌트 작성 문법)
- **SASS/SCSS**: CSS 전처리기 (스타일링)
- **LightningCSS**: 1.30.1 (CSS 번들링 및 최적화)

### 🔧 빌드 도구
- **esbuild**: 0.25.8 (초고속 JavaScript/TypeScript 번들러)
- **esbuild-sass-plugin**: 3.3.1 (SCSS 파일 처리)
- **tsx**: 4.20.3 (TypeScript 실행 도구)
- **Prettier**: 3.6.2 (코드 포매터)

### 📝 마크다운 처리 엔진
- **unified**: 11.0.5 (텍스트 처리 프레임워크)
- **remark**: 15.0.1 (마크다운 파서 및 변환기)
- **remark-parse**: 11.0.0 (마크다운 AST 파서)
- **remark-rehype**: 11.1.2 (마크다운을 HTML로 변환)
- **rehype**: HTML 처리 라이브러리 모음
  - **rehype-katex**: 7.0.1 (LaTeX 수식 렌더링)
  - **rehype-pretty-code**: 0.14.1 (코드 하이라이팅)
  - **rehype-autolink-headings**: 7.1.0 (제목 자동 링크)
  - **rehype-citation**: 2.3.1 (인용 처리)

### 🎯 마크다운 확장 기능
- **remark-gfm**: 4.0.1 (GitHub 풍 마크다운 지원)
- **remark-math**: 6.0.0 (수학 표기법 지원)
- **remark-breaks**: 4.0.0 (줄바꿈 처리)
- **remark-frontmatter**: 5.0.0 (메타데이터 처리)
- **remark-smartypants**: 3.0.2 (스마트 따옴표 변환)

### 🔍 검색 및 인덱싱
- **FlexSearch**: 0.7.43 (고속 전문 검색 엔진)
- **github-slugger**: 2.0.0 (URL 슬러그 생성)

### 🎨 시각화 및 그래픽
- **D3.js**: 7.9.0 (데이터 시각화, 그래프 뷰용)
- **Pixi.js**: 8.12.0 (2D 그래픽 렌더링)
- **Satori**: 0.16.2 (OG 이미지 생성)
- **Sharp**: 0.34.3 (이미지 처리)

### 🌐 웹 서버 및 네트워크
- **serve-handler**: 6.1.6 (로컬 개발 서버)
- **ws**: 8.18.3 (WebSocket, 핫 리로드용)
- **chokidar**: 4.0.3 (파일 시스템 감시)

### 📊 유틸리티 라이브러리
- **gray-matter**: 4.0.3 (YAML/TOML frontmatter 파싱)
- **js-yaml**: 4.1.0 (YAML 파서)
- **toml**: 3.0.0 (TOML 파서)
- **workerpool**: 9.3.3 (워커 스레드 풀)
- **async-mutex**: 0.5.0 (비동기 뮤텍스)

## 🔌 플러그인 아키텍처

Quartz는 3가지 타입의 플러그인으로 구성된 확장 가능한 아키텍처를 사용합니다:

### 🔄 Transformers (변환기 플러그인)
마크다운 파일을 처리하고 변환하는 플러그인들:

- **FrontMatter**: YAML/TOML 메타데이터 처리 (제목, 태그, 날짜 등)
- **GitHubFlavoredMarkdown**: GitHub 스타일 마크다운 지원 (테이블, 체크박스 등)
- **ObsidianFlavoredMarkdown**: Obsidian 전용 문법 지원 (위키링크, 임베드 등)
- **OxHugoFlavoredMarkdown**: Hugo 호환 마크다운 처리
- **RoamFlavoredMarkdown**: Roam Research 스타일 블록 참조
- **SyntaxHighlighting**: 코드 블록 문법 하이라이팅 (Shiki 기반)
- **TableOfContents**: 자동 목차 생성
- **CrawlLinks**: 링크 크롤링 및 해석 (상대 경로 처리)
- **CreatedModifiedDate**: 파일 생성/수정 날짜 추적
- **Description**: 페이지 설명 자동 생성
- **Latex**: LaTeX 수식 렌더링 (KaTeX 또는 MathJax)
- **Citations**: 학술 인용 처리
- **HardLineBreaks**: 강제 줄바꿈 처리

### 🚫 Filters (필터 플러그인)
콘텐츠를 필터링하여 출력에서 제외하는 플러그인들:

- **RemoveDrafts**: 초안(draft) 상태의 페이지 제외
- **ExplicitPublish**: 명시적으로 발행 표시된 페이지만 포함

### 📤 Emitters (생성기 플러그인)
최종 웹사이트 파일들을 생성하는 플러그인들:

- **ContentPage**: 개별 콘텐츠 페이지 생성
- **TagPage**: 태그별 페이지 목록 생성
- **FolderPage**: 폴더별 페이지 목록 생성
- **ContentIndex**: 검색 인덱스 및 사이트맵, RSS 피드 생성
- **AliasRedirects**: 페이지 별칭 리디렉션 설정
- **Assets**: 정적 자산(이미지, 파일) 복사
- **Static**: 정적 파일 처리
- **Favicon**: 파비콘 생성
- **ComponentResources**: CSS/JS 리소스 번들링
- **NotFoundPage**: 404 오류 페이지 생성
- **CNAME**: GitHub Pages용 CNAME 파일 생성
- **CustomOgImages**: 소셜 미디어용 이미지 생성

## 🧩 UI 컴포넌트 시스템

Quartz는 Preact 기반의 모듈화된 컴포넌트 시스템을 사용합니다:

### 📄 페이지 구조 컴포넌트
- **Head**: HTML head 태그 관리 (메타데이터, 스타일시트 로딩)
- **Header**: 페이지 상단 헤더
- **Footer**: 페이지 하단 푸터 (링크, 저작권 정보)
- **Body**: 메인 콘텐츠 영역

### 🧭 내비게이션 컴포넌트
- **PageTitle**: 사이트 제목 표시
- **Breadcrumbs**: 빵부스러기 내비게이션 (현재 위치 표시)
- **Explorer**: 파일 트리 탐색기 (폴더 구조 표시)
- **Search**: 전문 검색 기능 (Ctrl+K 단축키 지원)

### 📖 콘텐츠 표시 컴포넌트
- **ArticleTitle**: 개별 글 제목
- **ContentMeta**: 글 메타정보 (작성일, 수정일, 읽기 시간)
- **TagList**: 태그 목록 표시
- **TableOfContents**: 목차 (데스크톱 전용)
- **RecentNotes**: 최근 작성된 노트 목록

### 🔗 관계형 컴포넌트
- **Backlinks**: 현재 페이지를 참조하는 다른 페이지들의 링크
- **Graph**: 페이지 간 연결 관계를 시각화하는 그래프 뷰

### 🎛 인터랙션 컴포넌트
- **Darkmode**: 다크모드/라이트모드 토글
- **ReaderMode**: 읽기 모드 (집중 읽기를 위한 UI 단순화)
- **Comments**: 댓글 시스템 (Giscus 기반)

### 📱 반응형 컴포넌트
- **MobileOnly**: 모바일에서만 표시되는 컴포넌트
- **DesktopOnly**: 데스크톱에서만 표시되는 컴포넌트
- **ConditionalRender**: 조건부 렌더링 래퍼

### 🎨 레이아웃 컴포넌트
- **Flex**: 플렉스 박스 레이아웃 컨테이너
- **Spacer**: 여백 조정용 컴포넌트

### 📋 목록 컴포넌트
- **PageList**: 페이지 목록 표시
- **OverflowList**: 넘치는 항목을 접을 수 있는 목록

## 🎨 테마 및 스타일링

### 🌈 색상 시스템
현재 설정된 색상 테마:
- **라이트 모드**:
  - 주 배경색: #faf8f8 (밝은 회색)
  - 보조색: #284b63 (짙은 파랑)
  - 강조색: #84a59d (청록색)
- **다크 모드**:
  - 주 배경색: #161618 (어두운 회색)
  - 보조색: #7b97aa (밝은 파랑)
  - 강조색: #84a59d (청록색)

### 🔤 타이포그래피
- **헤더 폰트**: Schibsted Grotesk (Google Fonts)
- **본문 폰트**: Source Sans Pro (Google Fonts)
- **코드 폰트**: IBM Plex Mono (Google Fonts)

## ⚙️ 핵심 설정 파일

### 📝 quartz.config.ts
Quartz의 메인 설정 파일로 다음을 정의:
- **사이트 기본 정보**: 제목, URL, 로케일
- **플러그인 구성**: 사용할 변환기, 필터, 생성기 플러그인
- **테마 설정**: 색상, 폰트, 스타일
- **기능 설정**: SPA 라우팅, 팝오버, 분석 도구

### 🎭 quartz.layout.ts
페이지 레이아웃 구성을 정의:
- **공통 레이아웃**: 모든 페이지에 적용되는 헤더, 푸터
- **콘텐츠 페이지 레이아웃**: 개별 글 페이지의 구조
- **목록 페이지 레이아웃**: 태그, 폴더 페이지의 구조

## 🏗 빌드 프로세스

### 📋 빌드 단계
1. **콘텐츠 파싱**: 마크다운 파일을 AST(Abstract Syntax Tree)로 변환
2. **변환 적용**: Transformer 플러그인들이 순차적으로 콘텐츠 변환
3. **필터링**: Filter 플러그인이 불필요한 콘텐츠 제거
4. **페이지 생성**: Emitter 플러그인이 최종 HTML 페이지 생성
5. **자산 처리**: 이미지, CSS, JS 파일 최적화 및 번들링

### ⚡ 성능 최적화
- **워커 스레드**: 128개 이상의 파일 처리 시 멀티스레딩 활용
- **증분 빌드**: 변경된 파일만 다시 빌드
- **핫 리로드**: 개발 중 실시간 페이지 업데이트
- **코드 분할**: 필요한 JavaScript만 로드

## 🌟 주요 기능

### 📚 마크다운 지원
- **GitHub Flavored Markdown**: 테이블, 체크박스, 취소선 등
- **Obsidian 호환성**: 위키링크, 임베드, 태그
- **LaTeX 수학**: KaTeX를 통한 수식 렌더링
- **코드 하이라이팅**: 100+ 언어 문법 지원

### 🔍 검색 및 내비게이션
- **전문 검색**: 10ms 이내의 초고속 검색 (FlexSearch)
- **태그 검색**: #태그명으로 태그별 검색
- **그래프 뷰**: 페이지 간 연결 관계 시각화
- **백링크**: 현재 페이지를 참조하는 페이지 표시

### 📱 반응형 웹 디자인
- **모바일 최적화**: 터치 친화적 인터페이스
- **태블릿 지원**: 중간 크기 화면 최적화
- **데스크톱 레이아웃**: 사이드바와 멀티컬럼 배치

### 🚀 현대적 웹 기능
- **SPA 라우팅**: 페이지 간 즉시 전환
- **팝오버 미리보기**: 링크에 마우스 오버 시 내용 미리보기
- **다크 모드**: 자동/수동 테마 전환
- **PWA 지원**: 오프라인 접근 가능

### 🌐 다국어 지원
현재 지원되는 언어들:
- **한국어** (ko-KR)
- **영어** (en-US, en-GB)
- **일본어** (ja-JP)
- **중국어** (zh-CN, zh-TW)
- **기타**: 독일어, 프랑스어, 스페인어, 러시아어 등 25개 언어

### 📊 분석 및 SEO
- **사이트맵 생성**: 검색 엔진 최적화
- **RSS 피드**: 구독자용 피드 제공
- **소셜 미디어 이미지**: 자동 OG 이미지 생성
- **분석 도구**: Plausible Analytics 지원

## 🐳 Docker 지원

- **컨테이너화**: Node.js 설치 없이 Docker로 미리보기 가능
- **포트 설정**: 8080(웹서버), 3001(WebSocket)
- **볼륨 마운트**: 로컬 content 폴더와 연동

## 📂 프로젝트 구조

```
quartz/
├── content/                 # 마크다운 콘텐츠 파일들
├── quartz/                  # 핵심 Quartz 소스 코드
│   ├── components/          # UI 컴포넌트들
│   ├── plugins/            # 플러그인들 (transformers, filters, emitters)
│   ├── styles/             # 기본 스타일시트
│   ├── util/               # 유틸리티 함수들
│   └── build.ts            # 빌드 로직
├── docs/                   # 문서 (사용법, 가이드)
├── quartz.config.ts        # 메인 설정 파일
├── quartz.layout.ts        # 레이아웃 설정
├── package.json            # npm 의존성 및 스크립트
└── tsconfig.json           # TypeScript 설정
```

## 🎓 학습 추천 순서

### 📖 초급 개발자용
1. **마크다운 기초**: 마크다운 문법 익히기
2. **Git 기초**: 버전 관리 개념 이해
3. **Quartz 설치**: 기본 설정 및 첫 사이트 만들기
4. **콘텐츠 작성**: 기본적인 페이지 작성 및 링크 연결

### 🔧 중급 개발자용
1. **설정 커스터마이징**: quartz.config.ts 수정
2. **플러그인 이해**: 각 플러그인의 역할과 옵션
3. **레이아웃 수정**: 컴포넌트 배치 변경
4. **테마 커스터마이징**: 색상과 폰트 변경

### ⚡ 고급 개발자용
1. **TypeScript 개발**: 커스텀 플러그인 개발
2. **컴포넌트 개발**: 새로운 UI 컴포넌트 제작
3. **빌드 프로세스**: 내부 동작 원리 이해
4. **성능 최적화**: 빌드 시간 및 런타임 성능 개선

## 💡 활용 사례

- **개인 블로그**: 기술 블로그, 일상 블로그
- **디지털 가든**: 개인 지식 관리 시스템
- **문서 사이트**: 프로젝트 문서, API 문서
- **학습 노트**: 공부 내용 정리 및 공유
- **포트폴리오**: 개발자 포트폴리오 사이트
- **팀 위키**: 팀 내부 지식 공유 플랫폼

---

*이 문서는 Quartz 4.5.1 버전을 기준으로 작성되었습니다. 최신 정보는 [공식 문서](https://quartz.jzhao.xyz)를 참조하세요.*
