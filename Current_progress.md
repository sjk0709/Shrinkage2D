# Shrinkage2D

1. GPU : GTX770 (4G)
2. pytorch 사용

## Dataset
1. 256x256 사이즈의 mesh로 다양한 형상에 대해 수축공 해석
2. 256x256 사이즈의 feature는 현재 GPU spec에 너무 크기 때문에 128x128으로  줄였다. 


## Learning environment (모든 네트워크에 대한 공통된 환경)
1. feature_shape : [1, 128, 128]
2. label_shape : [1, 128, 128]
3. feature_type : torch
4. learning_rate : 1e-4


## jkcnn1 (batch_size : 100)

## jkvae1 (batch_size : 100)

## jkfcn1 (batch_size : 80)

## jkfcn2 (batch_size : 50)
jkfcn1 ( batch_size : 80 )과 비슷하나 조금 더 좋은 결과를 나타내는것으로 보인다.

## jkfcn4 (batch_size : 80)
학습중


## jkfcn5 (batch_size : 50)
현재 가장 좋은 결과 보여준다.



