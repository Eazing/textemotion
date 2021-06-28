# 2021-1학기 데이터분석캡스톤디자인 프로젝트 결과물

## 1. Introduction

### 주제선정배경
Facebook, Twitter, Instagram과 같은 다양한 Social Media의 발달로 사람들이 본인의 생각이나 감정을 짧은텍스트로 표현하는 일이 많아졌다. 텍스트에서 감정을 파악하는 모델을 통하여 Social Media 상의 우울증감지와 같은 다양한 활용이 가능해질 것이다.

### 주요 내용
과제의 주요 내용은 크게 네 가지로 나눌 수 있다.
 1. 영어 텍스트 데이터를 찾고 그 텍스트들을 전처리한다. 
 2. 전처리 완료된 텍스트에서 다양한 모델을 통해 감정을 추출한다.
 3. 각 모델에서 추출한 감정이 어느정도 정확도를 보이는지 검증한다.
 4. 어떤 모델이 가장 우수한 성능을 가지는지 비교한다.

### 최종 목표
최종 결과물의 목표는 3가지 이상의 모델을 비교하여 어떤 모델이 가장 정확도가 높은지 알아보는 것이다. 이를 통해 텍스트에서 감정을 추출하는 모델의 활용 가능성을 알아본다. 텍스트에서 감정을 파악하는 모델이 실제로 적용된다면, 다음과 같은 활용이 가능해질 것이다; Social Media 유저의 우울증 감지, 특정 키워드에 대한 감정(인식) 파악, 특정 기간 별 사람들이 감정 변화 관찰


## 2. Data Anlaysis

### 개발 환경 및 라이브러리
- 사용한 언어: Python
- 사용한 Tool: Google Colab
- 사용한 라이브러리: sklearn, numpy, padnas, nltk 등
 
### 데이터 전처리
- 텍스트 데이터베이스: ISEAR.csv (감정을 표현하는 문장 - 해당하는 감정)
- 감정 Label: 'joy', 'fear', 'anger', 'sadness', 'disgust', 'shame', 'guilt’
- Preprocessing
  - Tokenizes text
  - Clean sentence(Stop Words, Emoji, Emoticon, URLs, HTML tags, Number, Punctuation Marks)
  - Lower casing
  - TF-IDF
  - Word2Vec
- Training Dataser과 Test Dataset으로 나누어 각 모델에 대해 학습과 테스트 과정을 거쳤다.

### 모델 학습
총 8가지 Emotion Classification 모델에 대한 비교를 진행하였다. 선정한 모델은 다음과 같다; Multinomial Naive Bayes, Gaussian Naive Bayes, Logistic Regression, Support Vector Machine, Decision Tree, Random Forest, K-Nearest Neighbor, Multi-Layer Perceptron


## 3. Results

각 모델을 학습하여 그 성능을 테스트해 본 결과는 다음과 같다.
+ Multinominal Naive Bayes: Accuracy score is 0.639344262295082
+ Gaussian Naive Bayes: Accuracy score is 0.4426229508196721
+ Logistic Regression: Accuracy score is 0.6885245901639344
+ Support Vector Machine: Accuracy score is 0.6885245901639344
+ Desision Tree: Accuracy score is 0.5737704918032787
+ Random Forest: Accracy score is 0.6065573770491803
+ K-Nearest Neighbor: Accruacy score is 0.5081967213114754
+ Multi-Layer Perceptron: Accuracy is 0.7049180327868853

Multi-Layer Perceptron 모델이 약 0.705로 정확도가 가장 높았다.

## 4. Expected effect and Future works

### 기대효과 및 활용방안

텍스트에서 감정을 파악하는 모델을 통하여 다음과 같은 다양한 활용이 가능해질 것이다.
1. Social Media 유저의 정신 건강 상태 감지
  
  특정 유저의 감정 분석 결과에 sadness, fear, anger 등과 같은 부정적 키워드가 비정상적으로 많을 시 우울증을 의심해본다든지 유저의 정신 건강 상태에 대해 경고를 할 수 있다. 이에 그치지 않고 우울도가 높은 유저의 피드에 우울을 개선할 수 있는 상담이나 운동 등에 대한 광고 및 조언을 노출할 수 있다.
  
2. 특정 키워드나 인물에 대한 감정(인식) 파악
  
  기업에서 새로 출시한 상품이라든지, 스타나 정치인에 대한 사람들의 감정을 알아볼 수 있다. 이를 바탕으로 앞으로의 홍보 및 이미지 개선 방법에 참고할 수 있다.
  
3. 특정 기간의 사람들이 감정 변화 관찰

  선거, 연휴와 같은 이벤트가 있는 기간 또는 월별, 계절별로 사람들의 감정 변화를 관찰할 수 있을 것이다. 예를 들어 한여름의 폭염이 이어지는 기간에 사람들의 부정적 감정이 얼마나 커지는지 등을 알아볼 수 있을 것이다.


### 결론 및 제언

선정한 8개의 모델의 정확도를 모두 비교해봤을 때 Multi-Layer Perceptron 모델이 약 0.705로 정확도가 가장 높았다. 그 다음으로는 Logistic Regression과 Support Vector Machine의 정확도가 약 0.689로 비슷하게 높았다. 우리는 이 실험 결과를 통해, 텍스트에서 감정을 추출하는 모델이 약 70퍼센트 정도의 확률로 해당 텍스트의 감정을 추측해낼 수 있다는 것을 알 수 있었다. 우리는 Preprocessing 과정이나, Model의 세부 조건을 달리 하면서 70퍼센트 보다 우수한 성능을 가진 감정 추출 모델을 적용할 수 있을 것이다. 이러한 모델을 가지고 Social Media의 대중들의 반응이나, 특정 개인의 감정 변화를 알게될 수 있을 것이다.
