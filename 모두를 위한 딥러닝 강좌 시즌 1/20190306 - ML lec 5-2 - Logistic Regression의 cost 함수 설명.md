# 20190306 - ML lec 5-2 Logistic Regression의 cost 함수 설명

* Hypothesis가 Wx+b일 때에는 cost function : 2차 함수
* Logistic Regression일 때에는 울퉁불퉁한 2차 함수 모양으로 나타남
* 경사 하강면 알고리즘을 그대로 사용하면 Local Minimum에 빠질 수 있음 (찾고자 하는 건 Global Minimum)
* cost(W) = 1/m sigma c(H(x), y)
* c(H(x), y) = 
  - -log(H(x)) : y = 1
  - -log(1-H(x)) : y = 0
* 울퉁불퉁한 이유는 e term이 있기 때문인데, e와 상극인 log를 사용하여 펴 준다.
* 펴졌으므로 이제 경사 하강법을 사용할 수 있다.
* 예시
  - y = 1, H(x) = 1 ==> cost(1) = 0
  - y = 1, H(x) = 0 ==> cost(0) = infinity
  - y = 0, H(x) = 0 ==> cost(0) = 0
  - y = 0, H(x) = 1 ==> cost(1) = infinity
  - 시스템이 잘못 예측했을 때 패널티를 준다!

* if 조건이 너무 복잡하다! 줄일 수 있을까?
  - C: -ylog(H(x)) - (1-y)log(1-H(x))
  - y가 0과 1 중 하나이므로, 한 term은 0이 된다.

* Minimize Cost: Gradient Decent Algorithm
  - cost(W) = 1/m sigma (-ylog(H(x)) - (1-y)log(1-H(x)))

* 미분은 컴퓨터가 해 준다. 직접 계산 안 해도 된다.
