# Shrinkage2D

GPU : GTX770 (4G)
pytorch 사용

## Dataset
1. 256x256 사이즈의 mesh로 다양한 형상에 대해 수축공 해석
2. 256x256 사이즈의 feature는 현재 GPU spec에 너무 크다. $$$\rightarrow$$$ 128x128 interpolation 하여 줄였다. 


## Learning environment (모든 네트워크에 대한 공통된 환경)
1. feature_shape : [1, 128, 128]
2. label_shape : [1, 128, 128]
3. feature_type : torch
4. learning_rate : 1e-4


## jkcnn1 
1. bath_size : 100
2. 

## jkvae1 
1. bath_size : 100


## jkfcn1 
1. batch_size : 80

현재 가장 좋은 결과를 나타낸다. 

## jkfcn2 
1. batch_size : 50




