## PCA 와 AE
- 두개 모두 차원 축소를 하는 과정이 유사함.
- AE는 latent vector를 만들어서 차원 축소를 함.
- latent vector를 어떻게 만드느냐에 따라 Generative AI가 될 수도 있음.
- AE : reconstruct error는  latent 백터를 복원할 때 그 차이를 의미함
- AE : x랑 y를 비교하는 것은 mse도 됨(?)

## Transformer
### 인코더
1. self-attention : 필요한 정보에 집중
2. Multi-head attention
3. embeding
4. positioning embeding   

위는 중요도 순서이고,실제로는 3 -> 4 -> 1 -> 2 순서로 인코더가 진행됨 

## ResNet
1. 스킵커넥션 - 기울기 소실 문제 해결

## Inception(필터에 어텐션) (SENet은 채널에 attention)
1. 스킵커넥션을 쓰는데 여러 필터를 이용함.
2. 여러 필터가 모두 중요하진 않음. 이 필터 중 중요한 필터에 attention을 해야함
3. 일반적인 CNN에서는 각 필터와 채널에 attention을 취하지않고 동일하게 취급함
4. squeeze : 정보를 쥐어 짜내는걸 의미 (pooling으로)

자세한건 깃허브 참고  
https://github.com/MyungKyuYi/AI-class/blob/main/Variants_of_CNN

## 책
1. SE block : 610p

## 깃허브 내용
original cnn
depthwise cnn
pointwise cnn
inception
SENet