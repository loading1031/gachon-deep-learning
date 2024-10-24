
url = "http://archive.ics.uci.edu/ml/machine-learning-databases/auto-mpg/auto-mpg.data"




columns = ['mpg', 'cylinders', 'displacement', 'horsepower', 'weight', 'acceleration', 'model year', 'origin']



 df = pd.read_csv(url, delim_whitespace=True, names=columns, na_values='?') 



 
# 결측값 처리 (horsepower 컬럼에 결측값 존재)
df = df.dropna()

해당 소스를 활용하여 연비(Mile per gallen)를 예측 

mse를 구하라



1. ML (RF, DT, LR)

2. FCNN

3. 순환데이터로 변환후 CNN