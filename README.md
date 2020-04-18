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

# final term (team project) : parking lot space

deep neural network를 이용해서 주차장 공간안에 빈자리와 주차된 자리를 표시하고 빈 자리는 몇자리 남았는지 알려주는 프로그램

이미 만들어진 모델 VGG19를 사용하여 transfer learning(전이학습)함.

다른 층은 relu, selu를 적절히 사용.

* 만든 계기

![K-028](https://user-images.githubusercontent.com/52481037/79670000-ae0b3a80-81fa-11ea-8aee-63db4ad34353.jpg)

* training : 빈 공간, 주차된 공간을 잘라서 학습시킴 (0,1) ->주차장 전체 이미지와 주차공간의 csv파일이 들어오면 빈공간인지 아닌지 판별함

![K-027](https://user-images.githubusercontent.com/52481037/79670023-d2671700-81fa-11ea-92c0-2461604dbc23.jpg)

![K-029](https://user-images.githubusercontent.com/52481037/79670005-b2cfee80-81fa-11ea-8528-5e76a7fe9ac0.jpg)


* 결과물의 일부
![K-026](https://user-images.githubusercontent.com/52481037/79669819-53bdaa00-81f9-11ea-981d-7a8ef0371187.jpg)
