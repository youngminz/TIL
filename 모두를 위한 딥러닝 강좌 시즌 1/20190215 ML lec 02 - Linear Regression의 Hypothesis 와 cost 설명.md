# ML lec 02 - Linear Regression의 Hypothesis 와 cost 설명

# Regression (회귀)

- 리그레션 모델을 학습한다는 것은, 가설을 세우면서 하는 것
- (Linear) Hypothesis
    * H(x) = Wx + b
    * 세상에 있는 많은 현상들은 리니어하게 설명할 수 있기 때문에 큰 의미가 있음
- 데이터에 가장 잘 맞는 선을 찾는 것이 중요함
- 여러 가지 선(가설) 중 어떤 선이 가장 잘 맞는 선일까?
- 실제 데이터와 가설이 나타내는 점들과의 거리를 비교하는 방식
- Cost Function (Loss Function) : 우리의 트레이닝 데이터와 선이 얼마나 맞는지 확인하는 함수
    * cost(W, b) = 1/m (sigma i=1 to m (H(x_i) - y_i)^2)
    * (H(x) - y)^2 처럼 제곱을 해 주는 이유는, 거리가 먼 것에 패널티를 주기 위함임
- 목표 : Cost Function을 최소로 해 주는 W와 b를 구하는 것
