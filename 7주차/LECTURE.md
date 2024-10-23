1. CNN과 Dense layer 차이
2. RNN 특징
3. LSTM 특징 : 장기기억, 단기기억(cell) 분리
4. ResNet : skip connection, 잔차 학습
5. SE : 채널별로 중요도를 다르게 할 수 있음. (채널 어텐션, Average Pooling)
6. Inception : 서로 다른 필터 적용해서 서로 다른 특징을 동시에 추출 (1 x 1 필터)
7. depthwise seperable convolution : 채널을 나눠서 서로 다른 필터를 적용(depthwise)하고 다시 1x1으로 합침 (pair wise)
8. exception : pair wise를 먼저 하고 depthwise 적용
9. CBAM  : 채널 어텐션과 spatial 어탠션 (Pooling 사용)
10. spatial attention : 공간 집중
11. temporal attention : 시간 집중
12. Transformer
    - embedding : vector embeding
    - positional
    - self attention
    - Multihead attention
13. AE
    - 차원축소 (Manifold learning : 종이를 꾸겻다가 펴도 복원할 수 있음)
    - latent Vector
    - 인코더가 중요함
    - 입력값과 출력이 다른걸 reconstructor error 라 함.

책  
vision transform: 741p, 754p

```python
## AE_denoise에서 노이즈데이터로 기존 데이터를 복원시키도록 훈련시키는 방법도 있음
import numpy as np

import matplotlib.pyplot as plt

from keras.layers import Input, Dense

from keras.models import Model



# 데이터 생성: 노이즈가 없는 원본 데이터

np.random.seed(42)

data_size = 1000

original_data = np.sin(np.linspace(0, 2 * np.pi, data_size))



# 노이즈 추가

noise_factor = 0.2

noisy_data = original_data + noise_factor * np.random.normal(loc=0.0, scale=1.0, size=original_data.shape)



autoencoder = Model(input_layer, decoded)

autoencoder.compile(optimizer='adam', loss='mean_squared_error')



# 데이터 준비

x_train = noisy_data

x_train2 = original_data



# 모델 학습

autoencoder.fit(x_train, x_train2, epochs=100, batch_size=16, shuffle=True, verbose=0)



# validation dataset은 상관없음



# 노이즈 제거 후 데이터 예측

denoised_data = autoencoder.predict(noisy_test)
```