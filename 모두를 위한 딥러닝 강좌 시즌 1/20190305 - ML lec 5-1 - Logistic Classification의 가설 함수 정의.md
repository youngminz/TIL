# 20190305 - ML lec 5-1: Logistic Classification의 가설 함수 정의

* Classification 알고리즘 중 정확도가 아주 높은 알고리즘
* 그래서 아주 중요한 알고리즘임

* Regression과 다른 점은, 숫자를 예측하는 것이 아닌 카테고리를 예측하는 것
  - Spam mail detection: Spam or Ham
  - Facebook feed: Show or Hide - 내가 좋아하는 것들만 보여줌
  - Credit card fraudulent transaction detection: legitimate / fraud

* 0, 1 encoding
  - Spam detection: Spam (1) or Ham (0)
  - 0과 1으로 인코딩함

* Pass(1) / Fail(0) based on study hours
  - 2시간 Fail 
  - 3시간 Fail
  - 6시간 Pass
  - 이전에 배웠던 Linear Regrssion를 가지고 할 수도 있을 것 같음!
  - 0.5를 기준으로, 큰 값은 통과 작은 값은 불합격으로 하면 될 것 같음
  - Linear한 모델으로 그대로 학습시키면 극단적인 데이터가 있으면 잘못된 예측이 될 수 있음

* Use cases
  - 주식
  - 질병 진단

* Logistic Hypothesis
  - sigmoid function / logistic function g(z) = 1/(1+e^-z)
  - z가 무한정 커져도 1에 가까워진다.
  - z가 무한정 작아져도 0에 가까워진다.
  - H(X) = 1/(1 + e^(-W^T X))