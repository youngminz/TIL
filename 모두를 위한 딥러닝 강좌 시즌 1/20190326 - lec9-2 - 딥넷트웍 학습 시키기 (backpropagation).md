# 20190326 - lec9-2: 딥넷트웍 학습 시키기 (backpropagation)

## How can we learn W1, W2, b1, b2 from training data?

- Backpropagation으로 학습시킬 수 있음
- 틀렸을 때, 뒤에서 미분 값을 이용하여 파라미터를 자동으로 조정하는 알고리즘

## Backpropagation (chain rule)

- f = wx + b, g = ws, f = g+b
- dg/dw = x, dg/dx = w, df/dg = 1, df/db = 1

1. forward (w=-2, x=5, b=3)

f의 결과에 g가 얼마나 영향을 미치는가

- df/dw = df/dg * dg/dw = 1 * x = x = 5
- df/dx = df/dg * dg/dx = 1 * -2 = -2
- 각 파라미터에 의하여 f의 출력이 얼마나 변경되는지를 찾아내어 조정할 수 있음
- 이렇게 되면 많은 히든 레이어가 있다고 하더라도 동일한 방법으로 구할 수 있음

## Sigmoid
- g(z) = 1/(1+e^-z)

## 텐서플로우
- 모든 것은 그래프임
- 모든 것을 그래프로 만든 이유는 미분을 하기 위함임
- TensorBoard에서 볼 수 있음