# 20190429 - lec11-2: ConvNet Max pooling 과 Full Network

- Pooling Layer (Sampling)
    - 한 레이어씩 뽑아서 샘플링을 하고 쌓는 것을 말함
    - Max Pooling: 2x2 에서 가장 큰 값을 뽑아서 다운샘플링 하는 방법
    - 데이터 크기는 filter 크기와 stride 크기에 따라 변경됨

- Fully Connected Layer (FC Layer)
    - Contains neurons that connect to the entire input volume, as in ordinary NN