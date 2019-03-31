# 20190329 - lec10-1 - Sigmoid 보다 ReLU가 더 좋아

## NN for XOR
- Sigmoid와 같은 함수를 Activation Function이라고 함.
- 이 함수의 출력 값에 따라 넘길지 말지를 결정하기 때문
- Backpropagation은 86년도에 개발되었으나 2-3단에서는 잘 학습되나 9단이 넘어가면 학습 불가

## Chain Rule
- Sigmoid 함수를 많이 거치게 되면, 0에 아주 가까운 값을 여러 번 곱하기 때문에, 앞의 gradient가 작게 됨
- 2-3단 이상은 어려움
- Vanishing gradient 문제

## We used the wrong type of non-linearity
- Sigmoid는 항상 1보다 작음
- 0에서 1 사이에 있으므로, 0.9를 제곱해도 여러번 하면 작아짐
- ReLU - Rectified Linear Unit
- `tf.nn.relu` 함수 사용
- max(0, x)
- 마지막 단의 출력은 sigmoid를 사용함 (0-1 사이가 나와야 하기 때문)

## Activation Functions
- Sigmoid
- Leaky ReLU : max(0.1x, x)
- tanh : -1 ~ 1 사이
- Maxout
- ELU
- Leaky ReLU

