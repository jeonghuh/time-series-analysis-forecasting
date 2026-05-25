# time-series-analysis-forecasting
본 프로젝트는 시계열 데이터(Time-Series Data) 를 활용하여 항공 승객 수를 예측하는 프로젝트입니다.

대표적인 통계 기반 시계열 예측 모델인 ARIMA와 SARIMA 모델을 활용하여 시계열 데이터의 정상성(stationarity)을 검정하고, 차분(differencing), ACF/PACF 분석, 파라미터 최적화 및 계절성 예측을 수행하였습니다.

시계열 분석 및 예측 수업 프로젝트로 수행되었으며, 단순 예측이 아닌 통계적 검증 기반의 예측 프로세스 설계에 초점을 두었습니다.


## 1. 시계열 데이터 전처리
- Datetime Index 설정
- Train/Test 분리
- 시계열 데이터 시각화

## 2. 정상성(Stationarity) 검정

다음 기법을 활용하여 정상성 검정

- ADF Test (Augmented Dickey-Fuller Test)
- KPSS Test
- 1차 차분
- 2차 차분

## 3. ACF / PACF 분석

다음 데이터에 대한 자기상관 분석 수행

- 원본 데이터
- 1차 차분 데이터
- 2차 차분 데이터

이를 통해 아래를 추정
- AR(p)
- MA(q)
- 계절성 패턴



## 4. ARIMA 모델링

여러 ARIMA 모델을 비교 분석

- ARIMA(11,2,0)
- ARIMA(11,2,1)
- ARIMA(12,2,0)
- ARIMA(13,2,1)

평가 기준:

- AIC
- BIC(SBC)
- Ljung-Box Test


## 5. SARIMA 모델링

계절성을 반영하기 위해 SARIMA 모델을 적용
사용 내용:

- SARIMAX
- 계절성 파라미터 최적화
- Seasonal Forecasting 비교

**최종 우수 모델: SARIMA(0,0,2)(2,0,0,12)**
