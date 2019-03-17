# 20190315 - lec 07-2: Training/Testing 데이타 셋

## Performance evaluation: is this good?

- Training set를 가지고 평가한다면, 왠만하면 100점을 맞는다.
- 70% 정도의 데이터를 Training data set, 30%를 test set임. test set은 볼 수 없음.
- training set를 가지고 모델을 학습시킨 후, 테스트 데이터 셋을 가지고 평가한다.
- training set를 교과서, test set를 실전이라고 비유할 수 있음.

## Validation set
- alpha, lambda 값을 튜닝할 때, Validation set으로 사용한다.
- 실전 모의고사 같은 느낌.

## Online learning
- 100만 개의 training set는 너무 많으므로 10만 개씩 학습을 시킨다.
- 이러한 데이터는 괜찮은 데이터임. 추가 데이터로 학습을 시킬 수 있기 때문.

# Accuracy
- 실제 데이터의 y 값과 모델이 예측한 값이 몇 개가 맞았는지 체크
- 이미지 인식의 정확도는 95%를 넘고 있음
