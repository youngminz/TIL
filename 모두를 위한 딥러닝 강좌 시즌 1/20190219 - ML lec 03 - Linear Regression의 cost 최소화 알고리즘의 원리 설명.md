# 20190219 - ML lec 03 - Linear Regression의 cost 최소화 알고리즘의 원리 설명

- Hypothesis는 Wx+b로 주어지고, 이의 Cost Function, 즉 우리의 가설은 Cost Function으로 가정하였음.
- 과제는 Cost(W, b)를 줄이는 것.
- Cost 함수는 Linear Regression 을 넣을 때 2차 함수의 형태로 나옴. 6:10

Gradient Descent Algorithm
- 한국어로 경사 하강 알고리즘
- 주어진 Cost Function을 최소화함
- 많은 최소화 문제에 사용됨
- 파라미터가 더 많은 General Function에도 사용할 수 있음
- 어떻게 동작하는가?

원리
- 경사를 따라서 내려간다.
- 어디서 시작하던지 항상 Local Minimia으로 도착함

Formal Definition
- cost(W) = 1/2m (sigma i=1 to m (Wx_i - y_i) ** 2)
- W := W - alpha (d/dW cost(W)) and let alpha = 0.01

Convex Function
- Cost Function를 3차원으로 그렸는데, 여러 개의 Minima가 있는 경우 시작 점에 따라 결과가 다를 수 있음.
- 따라서 Gradient Descent Algorithm를 적용하기 전 반드시 Cost Function이 Convex Function인지의 여부를 확인해 보아야 함.