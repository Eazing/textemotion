2021-1학기 데이터분석캡스톤디자인 프로젝트 결과물

#과제 개요

Facebook, Twitter, Instagram과 같은 다양한 Social Media의 발달로 사람들이 본인의 생각이나 감정을 짧은텍스트로 표현하는 일이 많아졌다. 텍스트에서 감정을 파악하는 모델을 통하여 Social Media 상의 우울증감지와 같은 다양한 활용이 가능해질 것이다.
과제의 주요 내용은 크게 네 가지로 나눌 수 있다. 1) 영어 텍스트 데이터를 수집한다. 2) 수집한 텍스트를전처리한다. 3) 전처리 완료된 텍스트에서 다양한 모델을 통해 감정을 추출한다. 4) 각 모델에서 추출한 감정이 얼마나 정확도를 보이는지 검증한다. 영어 텍스트 데이터는 Labeling된 데이터베이스를 활용한다. 인식할 감정은 anger, fear, disgust, joy, sadness, surprise 총 6가지다. 텍스트 전처리 방법은 Tokenization, Noise removal, Stop words removal, Stemming을 포함하여 TF-IDF,wordtovec, fasttext 등의 방법으로 수행한다. 성능을 비교할 모델은 MLP, SVM, RNN(LSTM)이며, 모델 평가 방법은 Accuracy와 F score이다
최종 결과물의 목표는 3가지 이상의 모델을 비교하여 어떤 모델이 가장 정확도가 높은지 알아보는 것이다. 텍스트에서 감정을 파악하는 모델을 통하여 다음과 같은 다양한 활용이 가능해질 것이다; Social Media 유저의 우울증 감지, 특정 키워드에 대한 감정(인식) 파악, 특정 기간 별 사람들이 감정 변화 관찰
