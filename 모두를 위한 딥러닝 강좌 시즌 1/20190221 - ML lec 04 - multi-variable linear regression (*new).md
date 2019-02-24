# 20190221 - ML lec 04 - multi-variable linear regression (*new)

* Recap
    - Hypothesis
        * 함수에 대한 가설을 세운다. 
        * H(x) = Wx + b
    - Cost Function
        * 가설이 잘 되었는지를 평가하는 함수이다.
        * cost(W, b) = 1/m (sigma i=1 to m (H(x_i) - y_i) ** 2)
        * 예측한 값이 실제 값과의 차이를 제곱하여 합한 것
        * 일반적으로는 밥그릇 모양의 2차 함수가 나옴
    - Gradient Descent Algorithm: Cost를 최적화하는 알고리즘이다.
        * 경사면을 따라서 내려가는 알고리즘
        * Cost를 최적화하는 W와 b를 구한다.

- 하나의 Input Variable과 Y를 예측할 때는 간단함
- 변수가 여러 개인 경우
    * H(x) = Wx + b
    * H(x_1, x_2, x_3) = w1x1 + w2x2 + w3x3 + b
    * Cost(W, b) = 1/m sigma i=1 to m (H(x1_i, x2_i, x3_i) - y_i) ** 2
    * 예측한 값과 실제의 값이 얼마나 차이가 나는가를 알면 됨. 똑같음.
    * 행렬의 곱셈을 이용하면 편리하게 표현할 수 있음!
    * w1x1 + w2x2 + w3x3 + ... + wnxn = (x1 x2 x3) dot (w1 w2 w3)^T
    * H(X) = XW, X가 앞에 있는 것에 유의
- Many x instance
    * (x_1, x_2, x_3) 셋을 인스턴스라고 함
    * 여러 개의 데이터를 하나의 행렬로 표현하기 쉬움
    * 한 번에 전체의 행렬을 계산할 수 있음
    * Rank: [5, 3] * [3, 1] = [5, 1]; 선형대수를 잘 떠올려보자.... 중간의 3을 없애면 5, 1이 나온다
- WX vs **XW**
    - Lecture (theory): H(x) = Wx + b
    - Implementation (TensorFlow): H(X) = XW
