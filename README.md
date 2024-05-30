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
   - 5.8B 개의 파라미터를 가지고 있으며, Bloom모델을 기반으로 한국어와 다양안 언어호 추가 학습되었다.
   - 토크나이저의 크기는 32,000으로 다양한 언어와 어휘를 포괄한다.
     
<<https://huggingface.co/beomi/KoAlpaca-Polyglot-5.8B>>

----------------
### 3. Fine-tunning

 Koalpaca의 크기가 커서 로컬에서 진행하기에는 큰 한계가 있습니다. 본 프로젝트에서는 구글 코랩(Colab) 프로 플러스 버전의 A100 GPU를 사용했습니다.
