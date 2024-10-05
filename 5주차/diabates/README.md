## logistic
### 방법
> PCA를 사용하지 않고, 순수하게 로직스틱 회귀만을 이용하여 당뇨병 Outcome을 분류
### 결과
> Accuracy: 75.32%  
Confusion Matrix:  
[[79 20]  
 [18 37]]

## pca_logistic
### 방법
> PCA와 로직스틱 회귀를 이용하여 당뇨병 Outcome을 분류

### 결과
- n=2  
> Accuracy: 70.78%  
Confusion Matrix:  
[[81 18]  
 [27 28]]
- n=4
> Accuracy: 72.73%
Confusion Matrix:
[[81 18]
 [24 31]]
- n=6
> Accuracy: 77.27%  
Confusion Matrix:  
[[83 16]  
 [19 36]]
- feature는 총 8개 이므로 8부터는 의미 없음.

