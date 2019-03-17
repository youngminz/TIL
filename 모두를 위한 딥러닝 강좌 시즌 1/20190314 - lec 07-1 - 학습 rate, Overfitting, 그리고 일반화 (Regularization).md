# 20190314 - lec 07-1: 학습 rate, Overfitting, 그리고 일반화 (Regularization)

## 학습 rate
- Cost function를 최소화하는 값을 찾기 위하여 learning_rate를 정하였음
- step이 굉장히 클 경우, overshooting이 일어남. 이 상태에서는 학습이 일어나지 않음.
- step이 굉장히 작을 경우, 너무 오래 걸리며 local minimum에서 멈춤.
- 답은 없으며, 발산이 되지 않도록 잘 선택해야 함.

## 데이터 전처리 하기
- 데이터가 x1, x2 두 가지가 있는데, 두 개의 값의 형태가 굉장히 다르다면 왜곡된 등고선이 나타나게 됨
- normalize 해야 함. 많이 쓰이는 방법: zero-centered data, normalized data
- Standardization

## Overfitting
- 학습 데이터에 너무 딱 맞는 모델
- 실 사용에는 별로 맞지 않을 수 있음
- 오버피팅을 줄이는 방법
  * 트레이닝 셋 데이터를 늘리기
  * feature의 수를 줄이기
  * **Regularization**: weight를 너무 크지 않게 하기
  * 가장 일반적인 값은 Loss에 W^2를 더하는 것임
