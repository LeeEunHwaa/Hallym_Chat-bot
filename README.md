# Hallym_Chat-bot
한림대학교 챗봇 Da-Ara

![image](https://github.com/Kimsuyeon0809/Hallym_Chat-bot/assets/171135177/46204ddc-5bb4-4632-81b6-9c52048e8922)
-----------------


### 0. 프로젝트 개요 및 목적

<img width="726" alt="image" src="https://github.com/Kimsuyeon0809/Hallym_Chat-bot/assets/171135177/01593c25-c215-4543-aa71-78d55f7629e2">

 인공지능 기술 발달로 인공지능의 활용 능력이 곧 그 사람이나 기업, 단체의 능력으로 귀결되는 시대가 되었습니다. 특히 Open AI의 ChatGPT 발표 이후 LLM(Large Language Model)에 대한 연구가 활발하게 일어나며 전 분야에서 LLM 활용에 대한 중요성이 강조되고 있습니다. Enterprise Apps Today에서 발표한 통계에 따르면, 기술 분야 다음으로 Open AI를 가장 많이 활용하는 분야가 교육 분야일 정도로, 교육 분야에서의 LLM 활용 또한 활발하게 이루어지고 있습니다.

 이러한 동향에 발맞추어, 한림대학교에서 발표한 '한림대학교 혁신기획서'에 따르면 한림대학교 역시 AI 챗봇 개발을 통한 실시간 학습, 진로, 대학 생활 가이드 제공을 목표로하고 있습니다. 이에 맞게 본 프로젝트에서는 한림대학교에 대한 정보를 제공하는 AI advisor를 제작합니다.

 개인적인 차원에서는 정보를 찾기 어려워하는 학생들의 정보 접근에 대한 편리성을 제공합니다.

출처 <<https://www.enterpriseappstoday.com/stats/chatgpt-statistics.html>>

-----------------
### 1. 프로젝트 아키텍쳐
![image](https://github.com/Kimsuyeon0809/Hallym_Chat-bot/assets/171135177/1928fbc4-3a6e-456c-b097-4eebf92cb4e1)

-----------------

### 2. 한림 챗봇 Da-Ara의 Baseline Model
 Koalpaca-Polyglot-5.8B 모델을 선택하여 파인튜닝을 진행했습니다. 이 모델의 특징은 다음과 같습니다.
   - 한국어와 다국어를 지원하는 대규모 언어모델이다.
   - 5.8B 개의 파라미터를 가지고 있으며, Bloom모델을 기반으로 한국어와 다양안 언어로 추가 학습되었다.
   - 토크나이저의 크기는 32,000으로 다양한 언어와 어휘를 포괄한다.
     
<<https://huggingface.co/beomi/KoAlpaca-Polyglot-5.8B>>

----------------
### 3. Fine-tunning

 Koalpaca의 크기가 커서 로컬에서 진행하기에는 큰 한계가 있습니다. 본 프로젝트에서는 구글 코랩(Colab) 프로 플러스 버전의 A100 GPU를 사용했습니다.

 -----------------------

 ### 4. 




 ------------------------


### 5. 개발 화면 
한림대학교 챗봇 "DA-ARA" 구현화면 확인하기
(https://hallym-daara.netlify.app/)

----------------

### 6. 모든 기능 소개
> 1. 로그인 및 회원가입
성명, 학번, 비밀번호, 학과 입력시 회원가입이 가능하다.
학번과 비밀번호를 입력하여 로그인이 가능하다.
![폼](https://github.com/Kimsuyeon0809/Hallym_Chat-bot/assets/108513967/4dd90a36-ca49-4719-9b47-3b0fb732c297)

> 2. 메인페이지 (채팅)
한림대학교에 대한 질문을 입력하는 메인페이지이다.
![메인페이지](https://github.com/Kimsuyeon0809/Hallym_Chat-bot/assets/108513967/8f8629c8-1ef8-4cd6-8f42-d368ba4ad14e)

> 3. 챗봇 응답 음성 출력
우측 상단 스피커 아이콘으로 챗봇의 응답을 음성으로 출력할 수 있다.
![스피커](https://github.com/Kimsuyeon0809/Hallym_Chat-bot/assets/108513967/982a6d6a-8dc7-4cd6-bb9d-a4604acb7a4a)

> 4. 음성인식 텍스트 입력
좌측 하단의 마이크 아이콘을 눌러 음성인식 텍스트 입력이 가능하다.
![음성인식](https://github.com/Kimsuyeon0809/Hallym_Chat-bot/assets/108513967/945be1b0-c9da-4557-a965-ca05c5be6abc)

> 5. 이용가이드
한림대학교 챗봇 "DA-ARA" 이용가이드 
![이용가이드](https://github.com/Kimsuyeon0809/Hallym_Chat-bot/assets/108513967/0fe0a3be-a9d6-4e91-8e72-3a7b99d0e5a7)

> 6. 언어변경
한국어, 영어, 중국어, 일본어 총 4개 언어의 번역 기능을 제공한다. 해당 언어 클릭 시 현재까지의 대화 내용을 해당 언어로 번역할 수 있다.
![언어변경](https://github.com/Kimsuyeon0809/Hallym_Chat-bot/assets/108513967/313c864d-8cf1-44c4-a6d9-ed1c3ec1b686)

----------------

### 7. 사용API
|API|설명|
|------|---|
|SpeechSynthesis API|TTS API , 스피커를 통해 챗봇의 응답 음성 출력 가능|
|react-speech-recognition API|STT API, 마이크를 통해 음성인식 후 텍스트 입력 가능|
|구글번역 API|4개국어(한국어, 영어, 중국어, 일본어)를 지원|
|Flask API 프레임워크|인공지능 모델 개발 (Restful API로 요청과 응답을 Json 타입으로 통신하고, Json 값을 처리하여 사용자와 챗봇의 대화 내용을 웹에 출력하는 형태)|
