## ML
### ml_classification
- sex 원핫 인코딩시, `drop_first=True`로 하여 첫 번째 범주를 제거하여 다중공선성을 회피한다.
- 다중 공선성은 레이블의 각 범주가 상관관계가 있는 상황을 의미한다.
### ml_classification2
- sex 원핫 인코딩시, `drop_first=False`로 하여 정확도 측정한 코드. 
- True로 했을때보다 정확도가 0.01 정도 낮게 나온다. (SVM 기준)
### ml_classification3
- sex의 다다중공선성을 제거한 상태에서
- rings의 레이블을 0~29까지 다시 재배열한 경우이다. 
- ml_classification과 정확도면에서 변화가 없다.
### ml_regression
- StandardScaler() 적용
- 선형회귀 : 유의미한 차이 없음
- DT : mse가 0.2 더 낮음
- RF : mse 0.03 높음
- SVM : mse가 1.3 정도 더 낮음

## DL
### dl_classification
- rings는 정수형 레이블이다
- 그래서, `pd.get_dummies()` 아닌 `to_categorial()`을 적용함.
### dl_classification2
- dl_classification에 비교군이다.
- `pd.get_dummies()`을 적용함.
- categorical 인코딩 그래프가 더 안정적이다.
### dl_regression
- Y를 `pd.get_dummies()`로 인코딩
### dl_regression2
- Y를 `to_categorial()`로 인코딩
- dl_regression2가 훨씬 안정적인 그래프가 나옴.

## 분류 레이블이 연속적이지 않을 경우
1. y.value_count 
2. y를 원핫인코딩 후에 value_count 다시 확인
3. 1번과 2번을 비교한 값을 주석으로 다시 정리

##  index를 제외시키는 이유
1. 차원을 하나라도 더 축소시키기 위해 (차원의 저주 예방)