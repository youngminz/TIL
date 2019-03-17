# 20190311 - ML lec 6-2: Softmax classifier 의 cost함수

* sigmoid: 예측 값이 [0, 1] 사이에서 나오는 함수이며, 모두 더하면 p=1이 되는 것
* 즉, 각각을 확률로 볼 수 있는 것임
* a가 나올 확률 = 0.7, b = 0.2, c = 0.1 확률.
* one-hot encoding: Max만 1, 나머지는 0으로 처리해 주는 것, [0.7, 0.2, 0.1] => [1, 0, 0] 으로 처리

## Cross-entropy cost function

* cost function의 본질은 맞으면 0, 틀리면 큰 값을 주는 것
* 각각의 element를 곱해서 더한다.
  - [1 0] (element wise) [0 inf] = [0 0] => 0
  - [1 0] (element wise) [inf 0] = [inf 0] => inf

## Logistic cost vs cross entropy

* Logistic cost: C(H(x), y) = ylog(H(x)) - (1-y) log(1-H(x))
* Cross entropy: D(S, L) = -sigma_i (L_i log(S_i))
* 본질적으로 같다!
