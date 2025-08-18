### 코드 베이스 요약 및 학습 자료

이 코드 베이스는 **Obsidian**을 사용해 작성된 개인 지식 관리 시스템(Digital Garden)을 **Quartz**라는 정적 사이트 생성기로 웹에 게시하기 위한 프로젝트입니다.

핵심은 Obsidian으로 노트를 편하게 작성하고, 그 결과물을 Quartz를 통해 자동으로 웹사이트로 변환하여 공개하는 것입니다.

---

### 학습을 위한 추천 자료 (References)

이 프로젝트를 이해하고 발전시키기 위해 학습하면 좋은 주제와 관련 자료 목록입니다.

#### 1. Quartz (핵심 퍼블리싱 도구)

Quartz는 Obsidian 저장소(Vault)를 웹사이트로 만들어주는 핵심 도구입니다.

*   **[Quartz 공식 문서 (영문)](https://quartz.jzhao.xyz/)**: 설치, 설정, 커스터마이징 등 가장 정확하고 상세한 정보를 얻을 수 있는 곳입니다. **(필수)**
*   **[Quartz GitHub 저장소](https://github.com/jackyzha0/quartz)**: 다른 사람들의 이슈, 토론을 통해 문제 해결 팁을 얻거나 직접 기여할 수 있습니다.
*   **[Quartz Discord 채널](https://discord.gg/c6h5GAc6)
**: 실시간으로 질문하고 답변을 받을 수 있는 커뮤니티입니다.

#### 2. Obsidian (핵심 노트 작성 도구)

모든 콘텐츠가 작성되고 관리되는 곳입니다. Obsidian을 잘 다룰수록 웹사이트의 콘텐츠도 풍부해집니다.

*   **[Obsidian 공식 도움말 (한글 지원)](https://help.obsidian.md/Home)**: 기본 사용법부터 플러그인, 고급 기능까지 설명되어 있습니다.
*   **[생활코딩 - Obsidian 입문](https://www.youtube.com/watch?v=wN2Y3y_P3qI)**: Obsidian을 처음 사용하는 분들을 위한 쉬운 영상 가이드입니다.
*   **[Obsidian 포럼](https://forum.obsidian.md/)**: 전 세계 사용자들이 모여 팁, 플러그인, 활용 사례 등을 공유하는 공간입니다.

#### 3. 디지털 가든 (Digital Garden) (프로젝트 철학)

'디지털 가든'은 이 프로젝트의 결과물이 지향하는 개념입니다. 단순한 블로그가 아닌, 생각이 자라나고 서로 연결되는 유기적인 공간을 의미합니다.

*   **[A Brief History & Ethos of the Digital Garden (Maggie Appleton)](https://maggieappleton.com/digital-gardeners)**: 디지털 가든의 개념과 철학을 가장 잘 설명한 유명한 아티클입니다.
*   **[디지털 가든 개념 소개 (한글 블로그)](https://subinium.github.io/digital-garden-and-blog/)**: 디지털 가든이 블로그와 어떻게 다른지 쉽게 설명한 글입니다.

#### 4. 핵심 기반 기술

Quartz를 더 깊이 있게 커스터마이징하거나 문제 해결 시 필요한 기초 기술입니다.

*   **Markdown 문법**
    *   **[Markdown Guide (10분 입문서)](https://www.markdownguide.org/getting-started/)**: 웹사이트 콘텐츠 작성의 기본이 되는 마크다운 문법을 빠르게 익힐 수 있습니다.

*   **Git & GitHub**
    *   **[생활코딩 - Git 입문](https://opentutorials.org/course/2708)**: 버전 관리 및 GitHub Pages를 통한 배포를 위해 필수적인 기술입니다.
    *   **[Pro Git (한국어 번역)](https://git-scm.com/book/ko/v2)**: Git에 대해 더 깊이있게 배우고 싶을 때 참고할 수 있는 최고의 교재입니다.

*   **Node.js & npm**
    *   **[Node.js 공식 사이트](https://nodejs.org/)**: Quartz를 로컬 환경에서 실행하고 빌드하기 위한 런타임 환경입니다. 설치가 필요합니다.
    *   **[npm 이란 무엇인가? (한글 블로그)](https://programmingsummaries.tistory.com/375)**: Quartz의 플러그인 등 패키지를 관리하는 도구인 npm의 개념을 이해하는 데 도움이 됩니다.

---

### 추천 학습 순서

1.  **Obsidian & Markdown**: 먼저 노트 작성 도구와 기본 문법에 익숙해집니다.
2.  **Quartz 공식 문서**: 문서를 따라 기본 사이트를 설치하고 실행해 봅니다.
3.  **Git & GitHub**: 로컬에서 만든 사이트를 GitHub Pages 등을 통해 웹에 배포하는 방법을 학습합니다.
4.  **Quartz 커스터마이징**: 공식 문서를 참고하여 `quartz.config.ts`와 `quartz.layout.ts` 파일을 수정하며 나만의 사이트를 만들어 봅니다.