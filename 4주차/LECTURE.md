LSTM은 장기기억을 저장하는 cell 상태를 추가함.

rnn 은 숏기억만 저장하는 h1 상태만 다룸.

LSTM도 Gradient descendent vanishing문제가 발생해서 attention 개념이 나옴.


책 11장(gradient 폭발 문제): 434p -> 452p

domain adaptation: 도메인이 다른거에 대한 문제를 해결하는 것   
-> transfer learning으로 해결  
-> pretrained model 이용 (가져온 모델은 학습시키지 않음, 뒤에 추가(커스텀)한 레이어만 학습시킴)
-> fine tunning (가져온 모델까지 전체 학습 시킴)

데이터 정규화 : 숫자를 줄여 복잡도를 줄임

단어 임베딩 : 564p, 577p, 580p

14장: 577 ~ CNN 그냥 다 봐야함,  
GoogleNet: 601p, 602p: 1x1 커널을 사용하는 이유 셤 나옴 , 603p
VGGNet: 604p
ResNet
Xception: 깊이별 분리 합성곱(608p) + 일반 CNN과의 차이점(609p)
SENet

평가 방법이 선형적이지 않고 비선형적이라 파라미터가 늘어난다고 성능이 좋다고 확언할 수 없다.