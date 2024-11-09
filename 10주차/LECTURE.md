AE : reconstruction 에러 + KLDivergence 에러 최소화 
- 정보를 압축하는 것

PCA가 압축한 차원 정보는 알 수 없음

VAE의 목적 
- 기존의 데이터로부터 샘플링해서 표준편차를 얻어서 latent vector 생성
- latent vector로부터 정보 생성

GAN의 목적
- 기본 원리 숙지(변형은 소개만 )
- 생성형 모델 (VAE와 동일) 
- Mode collapse : 다양한 데이터를 생성하지 못하고 동일 데이터만 생성하는 것
    - 기울기 소실 문제
    - 원본 데이터의 bias

- Discriminative는 데이터의 분포를 구분하는 선을 찾아내는 것 - 인코더 : 초기에는 가짜데이터 구분하기 쉬움(정확도 높음)
- Generative는 주변의 데이터를 찾아냄(?) - 디코더 : 초기에는 가짜와 원본 오차가 큼

- 변형
    - DCGAN: conv layer 사용
    - CGAN : 조건을 제공해서 생성함 (condition)
    - Pix2Pix : 생성자와 판별자를 활용하여 이미지를 번역 (A-style을 -style로 바꾸는 하나의 방향성을 학습)
    - CycleGAN : A-Style->B-Style->A-Style로 다시 돌려보는 과정

라텐트 스페이스 크기
    - 클수록 복잡한 패턴을 학습할 수 있음 (근데 실제로는 안그럼)
    - 단, 학습이 힘듦 

Elbow: 목적함수 (Reconstruction error + KLLDivergence)

디퓨전 모델
- 원본에 노이즈를 넣어서 완전 노이즈 이미지를 생성 (forward propagatation)
- 노이즈 이미지로부터 원본을 복원(backward propagation)

### 책
752p, 753p, 754p, 772p, 774p (그림 11-17?), 776p, 779p, 780p, 793p