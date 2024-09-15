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
