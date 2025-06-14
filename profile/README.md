# 📚 서비스명: JEEUN-I (지은이)

---

## 🛠️ 기술 스택

### [Front-end]
- **Vue.js**: 3.5.3
- **Pinia**: 2.2.2
- **Vite**: 5.3.1

### [Back-end]
- **Python**: 3.13
- **Django**: 5.2.1

### [Database]
- **SQLite**

### [데이터 현황]
- 등록 도서: 약 50권  
- 등록 카테고리: 약 10개

---

## 1. 👥 팀 소개 및 역할 분담

| 이름      | 역할 및 담당 모듈                                           |
|----------|------------------------------------------------------------|
| 이예지     | ERD 설계, 회원가입/로그인 (BE), accounts 백 / 메인페이지 (FE + BE) / 문해력 테스트 및 도서 추천 (BE)        |
| 천예은     | 회원가입/로그인 (FE) / 독서 기록 (FE + BE) / 문해력 테스트 및 도서 추천 (FE)     |

---

## 2. 📝 프로젝트 개요

### (1) 💡 **프로젝트 주제 및 기획 배경**
- 과도한 스마트폰 사용과 전자책 보급으로 현대인의 문해력 저하가 사회 문제로 대두됨.
- 문해력 테스트와 독서 기록을 바탕으로, AI가 개인별 맞춤 도서를 추천하는 서비스 기획.

### (2) **서비스 한 줄 소개**
- 사용자 문해력 및 글쓰기 능력에 따라 도서를 추천하는 AI 독서 서비스

### (3) **프로젝트 목표**
- **⭐️ 목표:**  
  “개인의 문해력 수준을 진단하고, 그에 적합한 도서를 추천받아 문해력을 키울 수 있도록 돕는 것”

---

## 3. 🚩 **핵심 기능 소개**

### (1) **로그인/회원가입**
- 일반, 소셜(Kakao/Google), 게스트 로그인 제공  
- OAuth 2.0 기반 소셜 로그인

### (2) **독서 기록 및 도서 등록**
- 내가 읽은 책의 독서 기록 작성
- 서비스 내 미등록 도서는 알라딘 API/Google 이미지 검색으로 신규 등록 가능

### (3) **문해력 테스트**
- 국가문해교육센터 기준에 따라 단계별 문제 출제 (총 5단계)
- [단계별 세부 설명은 하단 표 참고]

### (4) **테스트 결과 기반 도서 추천**
- 문해력 테스트 결과를 바탕으로, AI가 “추천 도서/장르/설명/추천 이유/독서 팁” 제공 (OPENAI API 활용)

---

#### **문해력 테스트 문제 유형 예시**

| 단계 | 문항 수 | 문제 유형 |
|------|--------|----------------|
| 1단계 | 2      | 기초 연산, 낱말 고르기 |
| 2단계 | 3      | 맞춤법, 영어 표기, 짧은 추론 |
| 3단계 | 5      | 긴 글 주제 찾기, 문학/추론, 국어 사전, 자료 해석 |
| 4단계 | 2      | 복합 연산, 글 순서 |
| 5단계 | 3      | 비문학(법 규정), 안내문 추론, 한자어 이해 등 |

---

## 4. ⚙️ **서비스 아키텍처 및 ERD**

### (1) 시스템 아키텍처  
![지은이_아키텍쳐](https://github.com/user-attachments/assets/00fb720c-1c00-4aa3-995d-31b2328baac7)


### (2) 데이터베이스 모델(ERD)  
![image](https://github.com/user-attachments/assets/1dffbdaf-e878-4c4b-87b2-a73a853a22a1)

### (3) 도서 추천 알고리즘 설명
- **문해력 테스트 결과**와 **독서 기록**을 활용,  
  OPENAI GPT 기반 프롬프트 설계 →  
  추천 도서명/장르/설명/추천 이유/독서 팁 자동 생성  
- AI 추천 결과는 사용자에게 피드백 형식으로 제공

---

## 5. 🔗 **협업 툴 및 작업 방식**

- **Notion**: 일정 관리, 업무 분배, 회의록 등
- **GitHub**: Git flow, PR 리뷰, 이슈 관리  
    - Git Flow 및 Convention (이미지 첨부)
    - PR 리뷰 예시 (이미지 첨부)
- **Figma**: 화면/UX 설계 (와이어프레임/시안 이미지 첨부)

---

## 6. ✨ **생성형 AI 활용 내용**

- **OPENAI GPT API 활용**
    - 문해력 테스트 결과 기반 도서 추천 프롬프트 설계
    - 추천 도서명/장르/설명/이유/독서 팁 자동 생성

