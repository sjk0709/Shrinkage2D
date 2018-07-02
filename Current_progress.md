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

## Networks
### 파일 이름 설명
GC25_S3C40_jkfcn2_128_RX
1. GC25 : 금속재질
2. S3C40  -  S : 수축률(%)  | C : 한계고상률(%)
3. jkfcn2 : 네트워크 이름
4. 128 : input size가 128x128이다 
5. RX -  S(Sigmoid) | R(ReLU) |  X(없음)    Ex) RX -> (ConvNet - ReLU - DeconvNet - 없음)

### 진행상황
- 현재 jkfcn2 모델들이 가장 좋은 성능을 보여준다. 
- jkfcn5은 시각적으로 jkfcn2 보다는 부정확해보이나 앙상블에 포함해 볼만한다.
- 단순 jkcnn 시리즈 모델들은 쓰기 힘들 것으로 보인다.

- VAE 개선할 것
- ResNET 형식 네트워크 테스트 해보자. 
- GAN 시도해 볼 것

#### jkcnn1 (batch_size : 100)
#### jkcnn2 (batch_size : 100)
#### jkcnn3 (batch_size : 100)
* Conv 4 layer FC 2개 사용  ( conv : 64-64-128-128-256-256-256-512-512-512 ) - ( fc : 1200-output_size )
* pooling, dropout 사용
* batchnorm 사용안함 (메모리 절약)

#### jkcnn4 (batch_size : 100)



#### jkvae1 (batch_size : 100)

#### jkfcn1 (batch_size : 80)

#### GC25_S3C40_jkfcn2_128_SX (batch_size : 50)
jkfcn1 ( batch_size : 80 )과 비슷하나 조금 더 좋은 결과를 나타내는것으로 보인다.
현재 가장 좋은 결과를 보인다. 
* 앙상블에 포함해야 함

#### GC25_S3C40_jkfcn2_128_SS (batch_size : 50)
jkfcn1 ( batch_size : 80 )과 비슷하나 조금 더 좋은 결과를 나타내는것으로 보인다.
현재 가장 좋은 결과를 보인다. 
* 앙상블에 포함해야 함

#### GC25_S3C40_jkfcn2_128_RX (batch_size : 50)
jkfcn1 ( batch_size : 80 )과 비슷하나 조금 더 좋은 결과를 나타내는것으로 보인다.
현재 가장 좋은 결과를 보인다. 
* 앙상블에 포함해야 함

#### GC25_S3C40_jkfcn2_128_RS (batch_size : 50)
jkfcn1 ( batch_size : 80 )과 비슷하나 조금 더 좋은 결과를 나타내는것으로 보인다.
현재 가장 좋은 결과를 보인다. 
* 앙상블에 포함해야 함





#### jkfcn4 (batch_size : 80)
학습중


#### jkfcn5 (batch_size : 50)
* pooling, dropout 제거 (계산 및 메모리 절약)
* batchnorm 사용
* convolution에서 stride를 2로 설정함으로써 사이즈 줄여나감
* 결과 : 나쁘지 않다.
* 앙상블에 포함해야 함



