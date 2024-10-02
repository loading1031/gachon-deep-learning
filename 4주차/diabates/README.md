## 당뇨병 CNN hinge Loss 사용
### 목적 :   
> 이전에, CNN에 softmax가 아닌 svm을 결합하면, 성능이 향상된다는 포스트를 본적이 있음.  

출처 : https://m.blog.naver.com/winddori2002/222131106934
### 문제점 :
해당 코드는 파이토치이고, 텐서플로우로서는 SVM을 CNN에 하나로 합쳐서
SVM의 결과에 따라 CNN이 역전파 학습이 되게끔 하는 것은 어려웠음.

### 해결책 :
그래서, 기존 출력층 활성화 함수를 softmax -> linear로 바꾸고
손실함수 binary-crossentropy를 SVM에서 사용하는 hinge로 전환하여 
SVM처럼 출력이 되도록 바꿈.

### 파일 :
`cnn` : 기존 이진 분류의 cnn임. (softmax, binary-crossentrpy 사용)
`pretrained_cnn` : cnn에서 linear, hinge Loss를 이용하도록 변경 및 추가 레이어만 학습  
`fine_tuning` : cnn + pretrained_cnn을 모두 학습

### 결과 :
Dense 레이어를 추가하는 것보다 Conv 레이어를 추가했을 때, 성능 향상이 월등히 좋게 나옴. 
(Conv 1개에서 2개로 늘렸을 때만 확인했음)
  
다만, 파인튜닝시에 에포크를 증가할수록 안정화가 되지않고 값이 더 튀었음.