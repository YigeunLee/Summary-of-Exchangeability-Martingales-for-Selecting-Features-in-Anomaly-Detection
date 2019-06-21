# Summary-of-Exchangeability-Martingales-for-Selecting-Features-in-Anomaly-Detection
Summary of Exchangeability Martingales for Selecting Features in Anomaly Detection

Exchangeability Martingales for Selecting Features in
Anomaly Detection

비지도 비정상 탐색에서의 문제를 고려하였다 시계열에서 우리는 
Exchangeability Martingales 기반의 동일한 특징 패턴을 유지하는(iid 분포)
메소드를 개발하였다. 우리는 적용한다 이것을 여러 문제에(윈도우 서비스같은)

이것은 다음과 같은 아이디어에서 왔다 => 시계열에서 시간에 따른 iid 특징들의 식에서

문제설정
=>시계열에서의 데이터 셋 xt는 d차원의 벡터이다 이것은 트레이닝 페이즈일때
테스트 페이즈인 xt+1일 때 이것을 예측한다 이것이 비정상인지 아닌지

Exchangeability Martingales 을 사용한 Feature 선택
=>다음과 같은 특징은 제안된 내용에 적합하지 않다 만약 값들이 정규분포내의 데이터를 보이지 않을 경우
  우리는 다음과 같은 작업을 할 것이다. 우리는 특징 집합에서 iid를 보이지 않으면 그 특징 집합을 없앤다
  특징 시퀀스를 비교하기위해 다음을 할 수 있다

  1.p-value를 계산한다 특징 집합 (vt)를 Comformal Predictor(논문상에서는 K-NN을 사용)
  2.Betting Strategy를 사용하여 Martingale value를 계산한다 각 피쳐의 p-value를 위해
  3.만약 특정 Martingale value가 임계값을 넘어가면 그 값을 기각한다

Conformal Predictors
=>이것은 감싸진 스코어링 함수라고 할 수 있다.
Exchangeability martingales

=>MartingGales 는 현재 값과 다음 값의 기대값이 같다는 내용이다 이를 위해 다음과 같은 수식을 쓴다
  

Plug-in Martingales
=>Betting Function은 Kernel density estimation을 사용한다

kernel density estimation
=>비모수적(non-parametric)인 데이터를 근사화하여 pdf를 추정하는 기법
