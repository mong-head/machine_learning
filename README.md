# machine_learning
뇌및머신러닝강의를 들으면서 과제한 것과 과제를 위해 공부한 것 : hands-on-machine learning많이 참고

# midterm : regression, classification

1375?명정도의 환자의 데이터로 얼마나 이 환자가 알츠하이머 걸릴지 알아보는 과제

* 환자의 데이터 : 70여개의 cortical 두께 정보, 나이 등등

* regression : MMSE, ADAS13 수치를 찾아내는 것. 알츠하이머와 관련있는 숫자인듯

* classification : (뇌피셜) regression한 정보로 3개의 클래스로 나눔. 1단계가 안심단계일 것..? 3단계는 거의 걸릴 거라고 봄.


<순서>

1 data 처리 : imputer(median)-scaler(robust) -->pipeline
 - imputer : 없는 값 median으로 채워줌
 - scaler : 범위 벗어나는 값 제외
 
2 regression : rmse와 cross-validation score 비교함, linear,decision tree, randomforest 비교 후 randomforest선택

3 classification : svm, softmax, randomforest 비교 후 randomforest 선택

# midterm+ : randomforest vs. neural network

regression, classification 둘 다 randomforest가 더 나았다. 

다만, neural network는 층을 깊이 쌓은 deep neural network가 아니었음.
