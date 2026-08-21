# 🍱 [한끼상자] 1시간 시식회 웨비나 단계별 Skill 추천 가이드

> **브랜드 소개**: 갓 손질한 신선한 재료로 **20분 안에 완성하는 프리미엄 밀키트 브랜드 '한끼상자'**
> **웨비나 개요**: 가을 신메뉴 밀키트 시식 & 20분 요리 클래스를 결합한 1시간 라이브 웨비나
> **산출물 저장 위치**: `C:\Users\user\.gemini\antigravity\scratch\hankki-webinar``

---

## 📌 1. 단계별 Skill 매핑 종합표

| 진행 단계 | 단계별 핵심 과업 | 🟢 전역에 이미 설치된 Skill / 내장 기능 | 🔵 /find-skills로 새로 설치할 추천 Skill |
| :--- | :--- | :--- | :--- |
| **Step 1**<br>주제 후보 정리 | • 가을 제철 식재료 및 밀키트 트렌드 리서치<br>• 20분 조리 제약에 맞춘 3가지 웨비나 주제 도출 | • `antigravity-guide`<br>• `search_web` (최신 푸드 트렌드 검색)<br>• `invoke_subagent(research)` | • `brainstorming`<br>• `market-research`<br>• `trend-analysis` |
| **Step 2**<br>어울리는 연사 선정 | • 타깃 고객별 최적 연사 페르소나 설정<br>• 한식 셰프, 요리연구가, 내부 R&D 매칭 및 섭외안 작성 | • `search_web` (셰프/인플루언서 이력 조사)<br>• `agy-customizations` (브랜드 보이스 규칙 정의) | • `talent-scout`<br>• `speaker-curator`<br>• `persona-builder` |
| **Step 3**<br>상세페이지 작성 | • 신청 전환율(CRO)을 극대화한 랜딩페이지 카피<br>• 1시간 타임테이블, 사전 체험 혜택, 신청 CTA 구성 | • `permissioned-github` (페이지 배포/버전관리)<br>• 에이전트 마크다운/HTML 빌드 역량 | • `copywriting`<br>• `landing-page-generator`<br>• `cro-optimizer` |
| **Step 4**<br>홍보 포스터 생성 | • 가을 무드 & 20분 신메뉴 비주얼 프롬프트 설계<br>• 포스터 이미지 생성 및 채널별 디자인 에셋 가이드 | • `generate_image` (Imagen/DALL-E 기반 고해상도 생성)<br>• `agy-customizations` | • `image-prompter`<br>• `poster-design-assistant`<br>• `social-content-creator` |

---

## 🟢 2. 전역에 이미 설치된 Skill 및 내장 기능 상세

현재 Antigravity 환경에 전역(Built-in / Global)으로 설치되어 즉시 활용 가능한 스킬 및 에이전트 핵심 역량입니다.

### 1) `antigravity-guide` (전역 설치 Skill)
* **파일 위치**: `~/.gemini/antigravity/builtin/skills/antigravity_guide/SKILL.md`
* **핵심 기능**: Antigravity 에이전트의 워크플로우, 서브에이전트 조율, 슬래시 커맨드(/goal, /browser, /teamwork-preview 등) 가이드 제공.
* **본 프로젝트 활용**:
  - 웨비나 준비 작업을 서브에이전트(시장 조사 에이전트, 카피라이터 에이전트)로 병렬 위임하여 신속하게 결과물을 도출할 때 활용.

### 2) `agy-customizations` (전역 설치 Skill)
* **파일 위치**: `~/.gemini/antigravity/builtin/skills/agy-customizations/SKILL.md`
* **핵심 기능**: 프로젝트 전용 규칙(GEMINI.md, AGENTS.md) 정의 및 전용 커스텀 스킬 생성 가이드.
* **본 프로젝트 활용**:
  - 한끼상자의 브랜드 톤앤매너("20분 조리의 간결함", "신선한 프리미엄 식재료")를 에이전트 시스템 규칙으로 주입하여 모든 홍보 문구와 기획서의 일관성 유지.

### 3) `permissioned-github` (전역 설치 Skill)
* **파일 위치**: `~/.gemini/antigravity/builtin/skills/permissioned-github/SKILL.md`
* **핵심 기능**: GitHub 리포지토리 연동, 브랜치 생성, 변경 사항 커밋 및 PR 생성.
* **본 프로젝트 활용**:
  - 완성된 상세페이지 마크다운, 연사 섭외 기획서, 포스터 에셋을 팀 마케팅 리포지토리에 자동 버전 관리 및 배포.

### 4) Built-in Agent Tools (에이전트 내장 도구)
* **`generate_image`**: 가을 제철 식재료와 20분 조리 음식이 담긴 고해상도 홍보 포스터 그래픽을 직접 생성 (실제 hankki_webinar_poster.jpg 생성 완료).
* **`search_web`**: 최근 가을 시즌 인기 식품 트렌드(솥밥, 제철 버섯, 파인다이닝 밀키트) 및 활동 중인 셰프/인플루언서 탐색.
* **`invoke_subagent`**: 대규모 리서치 및 문서 작업을 백그라운드 병렬 작업으로 처리.

---

## 🔵 3. /find-skills로 새로 설치할 추천 Skill 상세

커뮤니티 및 오픈소스 스킬 에코시스템에서 /find-skills 또는 npx skills add 명령어로 설치하여 웨비나 기획 전문성을 극대화할 수 있는 추천 스킬입니다.

### [Step 1] 주제 후보 정리 단계
1. **`brainstorming`**
   - **설치 명령**: `npx skills add https://github.com/vercel-labs/skills --skill brainstorming`
   - **특징**: SCAMPER, 6-Thinking Hats 기법을 통해 20분 조리 시간이라는 제약 조건 속에서 가을 시즌성을 살린 차별화된 웨비나 주제 도출.
2. **`market-research` / `trend-analysis`**
   - **특징**: F&B 및 밀키트 시장의 최근 가을 소비 키워드, 타깃 페르소나의 라이프스타일 페인포인트 분석.

### [Step 2] 어울리는 연사 선정 단계
1. **`talent-scout` / `speaker-curator`**
   - **특징**: 행사 포맷(1시간 실시간 시연 + 시식)에 맞는 셰프/인플루언서 역량 평가 매트릭스 구성 및 최적 후보군 추천.
2. **`persona-builder`**
   - **특징**: 참가자 타깃군(3040 맞벌이 가구, 1인 가구 홈스토랑족)과 연사의 전문성/친화력 간의 시너지 분석 및 섭외 제안 메일 템플릿 생성.

### [Step 3] 상세페이지 작성 단계
1. **`copywriting`**
   - **설치 명령**: `npx skills add https://github.com/vercel-labs/skills --skill copywriting`
   - **특징**: PAS(Problem-Agitate-Solution) 및 AIDA 공식에 입각하여 20분 만에 셰프급 미식이 가능한 이유를 설득하는 고전환율 카피 작성.
2. **`landing-page-generator` / `cro-optimizer`**
   - **특징**: 1시간 타임테이블, 실시간 시식 키트 사전 배송 혜택, 신청 폼, 실시간 FAQ 등 랜딩페이지 UI/UX 블록 구성.

### [Step 4] 홍보 포스터 생성 단계
1. **`image-prompter` / `poster-design-assistant`**
   - **특징**: AI 이미지 생성 엔진(Imagen, Midjourney, DALL-E)에 최적화된 프롬프트(가을 조명, 플레이팅 질감, 스킬렛 김, 여백 구도) 엔지니어링.
2. **`social-content-creator`**
   - **특징**: 완성된 포스터를 바탕으로 인스타그램 피드(1:1), 스토리(9:16), 카카오톡 알림톡, 배너(16:9)용 맞춤 카피와 레이아웃 규격 가이드 제작.

---

## 💻 4. 스킬 설치 및 활용 방법 안내

### 1) 채팅창 슬래시 커맨드로 검색 및 설치
```text
/find-skills food marketing copywriting
/find-skills image prompt design
```

### 2) CLI 터미널에서 npx skills 명령어로 설치
```bash
# 1. 브레인스토밍 및 리서치 스킬 설치
npx skills add https://github.com/vercel-labs/skills -y -g --skill brainstorming

# 2. 카피라이팅 스킬 설치
npx skills add https://github.com/vercel-labs/skills -y -g --skill copywriting
```

---

## 📂 5. 프로젝트 생성 산출물 목록 (hankki-webinar)

1. `00_skill_recommendations.md` : (본 문서) 단계별 스킬 추천 및 전역/신규 설치 비교표
2. `01_webinar_topics.md` : 가을 신메뉴 20분 요리 클래스 웨비나 주제 후보 3선 & 1시간 타임테이블
3. `02_speaker_candidates.md` : 주제별 최적 연사 후보군(셰프/요리연구가/R&D팀장) 프로파일 및 섭외안
4. `03_detail_page.md` : 사전 등록 전환율을 극대화한 1시간 시식회 웨비나 상세페이지 전체 기획/카피
5. `04_poster_prompts.md` : AI 이미지 생성 프롬프트 및 채널별 비주얼 디자인 가이드
6. `hankki_webinar_poster.jpg` : 실제 생성된 가을 신메뉴 20분 요리 클래스 고해상도 홍보 포스터