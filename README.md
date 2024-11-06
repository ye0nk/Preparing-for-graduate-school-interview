# 인하대 인공지능대학원 면접 대비
---


## Interview Questions

<details>
<summary><a href="./answers/1-statistics-math.md"><strong>📈 통계/수학</strong></a></summary>

- 고유값(eigen value)와 고유벡터(eigen vector)이 무엇이고 왜 중요한지 설명해주세요.
```python
  행렬 A의 고유벡터는, 행렬 A에 의해 변환되었을 때 방향이 변하지 않고 단지 크기만 변하는 벡터를 말한다
  Av=λv에서 v (영벡터 아니어야 함)
  고유값은 λ (고유벡터 v가 변환될 때 그 크기가 얼마나 변하는지...)
```
- 샘플링(Sampling)과 리샘플링(Resampling)이 무엇이고 리샘플링의 장점을 말씀해주세요.
```python
  샘플링은 전체 모집단에서 데이터를 추출하는 거,특히나 모집단을 대표할 수 있도록 신중하게 선택되어야 함
  리샘플링은 기존의 샘플 데이터에서 새로운 샘플을 반복적으로 추출하여 통계적 분석을 수행하는 방식
  리샘플링에는 다음과 같은 방법이 있다
  - 교차 검증 (Cross Validation) : 모델의 성능 평가를 위해 데이터를 여러 번 분할하여 훈련과 테스트를 반복! 과적합 방지, 모델의 일반화 성능 평가
```
- 확률 모형과 확률 변수는 무엇인가요?
```python
  확률은 불확실성을 표현하는 수단, 이러한 불확실성을 확률로써 개량화하기 위해 확률함수로써 수학적으로 만든 모형이 확률 모형이다
  이는 어떤 실험이나 현상에서 가능한 모든 결과와 그 결과가 발생할 확률을 설명한다.
  확률 모형은 표본 공간, 확률 분포라는 두 가지 구성 요소로 이루어졌다!

  확률 변수는 확률 모형에서 정의된 함수
  쉽게 말하면 확률로 표현하기 위한 event를 정의하는 것
  어떤 것을 확률로 표현할 것인지에 대해 다양하게 정의가 가능하여 <변수>라는 용어를 사용한다
  (이산과 연속 확률 변수로 나뉨)
```
- 누적 분포 함수와 확률 밀도 함수는 무엇인가요? 수식과 함께 표현해주세요.
```python
  확률 밀도 함수는 연속 확률 변수의 분포를 설명하는 함수로, 특정 값에서의 확률 밀도를 나타낸다.
  누적 분포 함수는 확률 변수가 특정 값 이하일 확률을 타나내는 함수, 확률 밀도 함수를 적분하여 구할 수 있다
```
- 조건부 확률은 무엇인가요?
```python
   조건부 확률은 어떤 사건 A가 이미 일어난 상황에서 다른 사건 B가 일어날 확률을 의미한다
   즉 사건 B가 사건 A에 의해 영향을 받을 때의 확률을 계산할 것
```
- 공분산과 상관계수는 무엇일까요? 수식과 함께 표현해주세요.
```python
   공분산(Covariance)는 두 확률 변수 사이의 관계를 측정하는 지표로, 두 변수가 함께 어떻게 변하는지를 나타낸다
   즉 한 변수가 증가할 때 다른 변수가 증가하거나 감소하는 경향을 평가한다
   Cov(X,Y)=E[(X−E(X))(Y−E(Y))]

   상관계수는 공분산을 정규화하여 두 확률 변수 사이의 선형 관계를 1과 -1 사이의 값으로 표현한다
   상관계수는 공분산과 달리 단위에 의존하지 않기 때문에 비교적 직관적으로 두 변수의 관계 강도를 파악할 수 있다!
```
- 신뢰 구간의 정의는 무엇인가요?
```python
  신뢰구간은 모집단의 모수를 포함할 것으로 예상되는 값의 범위를 특정 신뢰 수준 하에 제시한 것이다
  즉 표본 데이터를 이용해 계산한 추정치가 모집단의 실제 값(모수)를 포함할 확률이 높은 구간을 의미한다
  보통 신뢰 수준과 함께 나타나며, 신뢰 수준은 이 구간이 모집단의 실제 모수를 포함할 확률을 의미한다.
```
- p-value를 모르는 사람에게 설명한다면 어떻게 설명하실 건가요?
```python
  신뢰구간은 모집단의 모수를 포함할 것으로 예상되는 값의 범위를 특정 신뢰 수준 하에 제시한 것이다
  즉 표본 데이터를 이용해 계산한 추정치가 모집단의 실제 값(모수)를 포함할 확률이 높은 구간을 의미한다
```
- R square의 의미는 무엇인가요?
```python
  R², 또는 결정계수(R-Squared)는 회귀 분석에서 사용되는 통계량으로,
  독립 변수가 종속 변수의 변동을 얼마나 잘 설명하는지를 나타낸다.
  즉, R²는 회귀 모델이 데이터를 얼마나 잘 설명하는지를 평가하는 지표이다.
```
- 평균(mean)과 중앙값(median)중에 어떤 케이스에서 뭐를 써야할까요?
```python
   평균은 데이터가 고르게 분포되어 있고 이상치가 없을 때 더 신뢰할 수 있다.
   하지만 이상치가 있으면 평균이 그 값에 의해 크게 영향을 받아 데이터의 중심을 제대로 반영하지 못할 수 있다.
   중앙값은 이상치나 비대칭 분포가 있는 경우 더 적절하다. 극단적인 값이 있더라도 중앙값은 그 영향을 받지 않기 때문에 데이터의 중심을 더 잘 나타낸다.
```
- 중심극한정리는 왜 유용한걸까요?
```python
   중심극한정리는 확률론에서 매우 중요한 개념으로, 표본 크기가 충분히 크면 어떤 분포를 따르는 모집단에서 표본을 추출하더라도,
   표본 평균의 분포가 정규분포에 가까워진다는 것을 의미한다!
   다시 말해, 모집단의 분포 형태에 관계없이 표본 평균의 분포는 표본 크기가 커질수록 점점 정규분포를 따르게 된다.
   중심극한정리는 다양한 형태의 모집단에서 표본을 추출해도, 표본 평균이 정규분포를 따르게 만들어 준다.
   이로 인해 모집단의 분포를 알지 못해도 표본 평균의 분포를 예측할 수 있습니다.
```
- 엔트로피(entropy)에 대해 설명해주세요. 가능하면 Information Gain도요.
```python
   엔트로피는 정보 이론에서 사용되는 개념으로, 불확실성 또는 혼란의 정도를 측정하는 지표이다.
   주로 확률 분포의 다양성을 측정하거나, 데이터의 예측 가능성을 평가하는데 사용된다.
   쉽게 말하면 데이터의 무질서도를 측정, 값이 높을 수록 불확실성이 커진다!

  정보 이득 (Information gain)
  정보이득은 결정 트리와 같은 알고리즘에서 특정 속성을 사용해 데이터 집합을 분할할 때, 엔트로피가 얼마나 감소하는지를 측정하는 지표이다
  즉 특정 속성을 기준으로 데이터를 나눴을 때 데이터의 불확실성이 얼마나 줄어드는지 나타낸다!
```
- 어떨 때 모수적 방법론을 쓸 수 있고, 어떨 때 비모수적 방법론을 쓸 수 있나요?
```python
   모수적 방법론은 모집단의 분포에 대해 특정한 가정을 하고 데이터를 분석하는 기법
   예를 들어 데이터가 정규분포를 따르는 것으로 가정하고 통계적 분석을 수행하는 경우가 대표적
   모수적 방법론은 데이터의 분포가 알려져 있을 때/ 표본 크기가 충분히 클 때/모집단의 분포에 대한 강한 가정이 성립할 때/ 등에서 사용

   비모수적 방법론은 데이터의 분포에 대한 가정이 필요하지 않은 분석 방법이다
   이 방법은 데이터가 특정한 분포를 따르지 않거나, 분포를 알 수 없을 때 유용하다
```
- “likelihood”와 “probability”의 차이는 무엇일까요?
```python
   확률(probability)은 주어진 모수에 대해 데이터가 발생할 확률
   가능도(Likellihood)는 주어진 데이터에 대해 모수가 그 데이터를 얼마나 잘 설명하는지를 평가
   예를 들어서 동전을 여러 번 던져 7번 중 5번 앞면이 나왔다고 가정하면
   확률은 5/7
   가능도는 특정한 모수 p가 주어졌을 때, 관측된 데이터 "7번 중 5번 앞면이 나옴"을 얼마나 잘 설명하는지를 평가
   L(p|X=5)
```
- 통계에서 사용되는 bootstrap의 의미는 무엇인가요.
```python
   부트스트랩은 통계적 추정의 신뢰성을 평가하기 위해 사용되는 비모수적 방법론
   특히 모집단의 분포에 대한 강한 가정을 하지 않고, 표본 데이터만을 사용해 모집단의 특성을 추정할 수 있는 강력한 기법이다.
   부트스트랩은 주어진 표본 데이터로부터 반복적으로 새로운 표본을 생성하여, 통계적 추정값(예: 평균, 분산, 신뢰구간 등)의 분포를 추정하는 방법이다.
```
- 모수가 매우 적은 (수십개 이하) 케이스의 경우 어떤 방식으로 예측 모델을 수립할 수 있을까요?
```python
   1. 간단한 모델 사용 : 선형 회귀, 로지스틱 회귀, k-최근접 이웃(KNN), 의사결정트리와 같은 단순한 모델을 사용하는 것이 좋습니다.
   2. 규제(Regularization) 기법 사용: 과적합을 방지하기 위해 L1, L2 규제 방법을 적용하여 모델의 복잡성을 줄일 수 있다
   3. 데이터 증강 : 데이터를 오히려 인위적으로 늘린다
```
- 검정력(statistical power)은 무엇일까요?
```python
   어떤 통계적 검정이 실제로 대립가설이 참일 때 이를 올바르게 검출할 확률을 의미한다.
   쉽게 말해, 검정력은 참인 효과를 감지할 수 있는 능력을 나타낸다.
   검정력의 의미: 검정력이 높을수록, 실제로 효과나 차이가 존재할 때 이를 발견할 가능성이 커진다.
```
- missing value가 있을 경우 채워야 할까요? 그 이유는 무엇인가요?
```python
   결측치가 있는 데이터를 그대로 사용하면 통계 분석, 머신러닝 모델링에서 왜곡된 결과를 초래할 수 있다
   특히 일부 알고리즘은 결측치를 허용하지 않기 때문에 데이터 전체가 무효화될 수 있다.
   결측치를 적절히 채우면 모델의 성능을 높일 수 있다. 결측치로 인해 모델이 학습할 수 있는 정보가 제한되거나, 예측의 정확도가 떨어질 수 있기 때문이다.
```
- 아웃라이어의 판단하는 기준은 무엇인가요?
```python
   아웃라이어는 데이터에서 다른 데이터 포인트와 비교해 극단적으로 벗어난 값을 의미한다.
   통계적 기준으로는 사분위 범위(IQR)에서 Q1-3*IQR보다 작거나, Q3+3*IQR보다 크면 보통 outlier라고 칭한다
   또는 데이터가 정규분포를 따른다고 가정할 떄, 평균에서 k개의 표준편차 이상 떨어진 값을 아웃라이어로 간주한다
```
- 필요한 표본의 크기를 어떻게 계산합니까?
```python
   표본 크기를 계산하는 방법은 연구의 종류에 따라 다르다
   평균의 차이를 비교할 때 : t 검정
   비율의 차이를 비교할 떄 : z 검정
   
```
- Bias를 통제하는 방법은 무엇입니까?
```python
   연구 설계 단계에서 Bias 통제 : 무작위 할당 (Randomization) - 실험군과 대조군에 참여자를 무작위로 배정해 그룹 간 차이 최소화, 무작위화는 선택 편향(Selection Bias)를 줄임
   데이터 수집 단계에서 Bias 통제 : 표준화된 측정 방법(Standardized Measurement) - 모든 데이터를 일관된 방식으로 수집해 측정 편향 (Measurement Bias)을 줄인다
   데이터 분석 단계에서의 Bias 통제 : 혼란 변수 (Confounding Variable) 통제 - 혼란 변수가 연구 결과에 영향을 미치지 않도록 다변량 분석, 공변량 분석을 사용해 통제
   
```
- 로그 함수는 어떤 경우 유용합니까? 사례를 들어 설명해주세요.
```python
   데이터가 크기 차이가 클 때나 지수적 증가가 있는 경우 유용하다.
   예를 들어서 금융 데이터를 분석할 때
   금융 분야에서는 기업의 매출, 시장 규모, 자산 등 다양한 변수가 매우 큰 범위를 가질 수 있다. 어떤 회사의 매출은 수백만 달러일 수 있지만, 또 다른 회사의 매출은 수십억 달러에 이를 수 있다
   로그 변환을 통해 이런 큰 차이를 줄이면 데이터가 더 균형 있게 분포되면, 분석하기 쉬워진다
   예를 들어 히스토그램을 그릴 때 로그 변환을 적용하면 극단적인 값들로 인해 왜곡되지 않은 분포를 볼 수 있다!
```
- 베르누이 분포 / 가우시안 정규 분포  / 카이제곱 분포 / 에 대해 설명해주세요.
```python
  베르누이 분포는 두 가지 결과(성공 혹은 실패)만 가능한 이산 확률 분포이다. 각각의 결과가 발생할 확률을 기반으로 한다. 베르누이 분포의 확률 변수 X는 1과 0만을 가질 수 있다
  가우시안 정규 분포는 연속 확률 변수로, 데이터가 평균값을 중심으로 종 모양의 대칭적인 분포를 따른느 경우를 설명한다. 이는 많은 자연현상에서 나타나는 일반적인 분포이다
  카이 제곱 분포는 연속 확률 분포로, 독립적인 표준 정규 분포 변수의 제곱의 합으로 정의된다. 카이제곱 분포는 자유도에 따라 모양이 달라진다.
```

</details>

<details>
<summary><a href="./answers/2-machine-learning.md"><strong>🤖 머신러닝</strong></a></summary>

- 알고 있는 metric에 대해 설명해주세요. (ex. RMSE, MAE, recall, precision ...)
```python
   RMSE는 회귀 모델의 성능을 측정하는 데 사용된다. 예측 값과 실제 값의 차이를 제곱한 평균의 제곱근을 계산한다.
   MAE는 예측 값과 실제 값의 차이의 절대값 평균을 계산한다. 회귀 모델의 성능을 측정하는 또 다른 지표이다.
   Precision은 모델이 True Positive로 예측한 것 중 실제로 True인 비율을 의미한다. 특히 양성 클래스에 대한 정확도를 측정하는 데 유용하다. TP / (TP+FP)
   Recall은 실제로 True인 것 중에서 모델이 True로 예측한 비율을 의미한다. TP / (TP + FN)
   F1 Score는 Precision과 Recall 사이의 균형을 평가하는 지표이다. precision과 recall의 조화 평균을 계산한다. F1 score = 2 * { (Precision X Recall) / (Precision + Recall) }
   R-squared(결정계수)는 회귀 분석에서 모델이 데이터를 얼마나 잘 설명하는지를 나타내는 지표이다. 0에서 1 사이의 값을 가지며, 1에 가까울수록 모델이 데이터를 잘 설명하는 것을 의미한다. 
```
- 정규화를 왜 해야할까요? 정규화의 방법은 무엇이 있나요? (🥲 내 논문 주제...)
```python
   머신러닝 알고리즘(특히 경사 하강법 기반 알고리즘)은 특성(feature) 값의 범위가 매우 다르면 학습이 제대로 이뤄지지 않을 수 있다.
   예를 들어 하나의 특성의 값이 0~1 사이인데, 다른 특성의 값이 0~10000 사이라면 큰 범위를 가진 특성이 모델 학습에 더 큰 영향을 미치게 되어 잘못된 가중치를 학습할 가능성이 있다.
   특히 경사 하강법 기반 알고리즘의 경우 정규화를 하면 학습 속도가 빨라지도 알고리즘이 더 잘 수렴하게 된다.
   정규화된 데이터는 최적의 해를 찾는 과정에서 균형 잡힌 경로로 수렴하도록 도와준다.
   심지어 일부 알고리즘은 특성의 크기 차이로 인해 성능이 저하될 수 있다. 정규화를 하면 이러한 문제를 방지하여 모델 성능이 향상될 수 있다.

   정규화 방법
   Min-Max 정규화 : 데이터를 (대체로) 0~1로 변환하는 방법. 최소값을 0, 최대값을 1로 변환하며, 나머지 값은 비례적으로 조정한다.
   Z-Score 정규화 : 데이터를 평균 0, 표준편차 1로 변환하는 방법. 데이터가 정규 분포를 따를 때 효과적!
   Robust 정규화 : median과 사분위 범위 (IQR)를 사용하여 정규화하는 방법이다. 이상치에 덜 민감하다.
```
- Local Minima와 Global Minimum에 대해 설명해주세요.
```python
   Global Minimum은 전역 최소값. 함수의 모든 가능한 값 중 가장 낮은 값, 최적화 문제에서 우리가 궁극적으로 찾고자 하는 지점!
   Local Minima는 특정 영역 내에서 가장 낮은 함수 값을 가지는 지점을 의미, but 다른 영역에 더 낮은 값이 존재할 수도 있다!
```
- 차원의 저주에 대해 설명해주세요.
```python
   차원의 저주는 고차원 공간에서 발생하는 여러 가지 문제를 의미한다. 데이터 분석 및 머신러닝에서 데이터의 차원이 증가할수록 발생하는 현상으로, 학습 및 일반화 성능에 부정적인 영향을 미칠 수 있다.
   쉽게 정리하자면 변수가 늘어남에따라 차원이 커지면서 분석을 위한 최소한의 필요 데이터 건수가 늘어나면서 예측이 불안정해지는 문
   차원의 저주가 발생하는 이유
   1. 데이터의 희소성 (Sparsity) : 차원이 증가할수록 데이터 포인트들이 서로 멀리 떨어져 분포하게 된다
   2. 거리 측정의 신뢰도 감소 : 머신러닝의 여러 알고리즘 (특히 K-최근접, K-means)은 거리 측정을 기반으로 동작한다. 그러나 차원이 높아지면 데이터 포인트들 간의 거리가 점점 비슷해져서 유사성 측정이 어렵다
   3. 데이터 필요량의 증가 : 차원이 증가할수록 고차원 공간을 대표하기 위해 필요한 데이터의 양이 기하급수적으로 증가한다
   4. 모델의 복잡도 증가 : 차원이 증가하면 모델의 복잡도가 증가하여 과적합(overfitting)의 위험이 커진다
```
- dimension reduction기법으로 보통 어떤 것들이 있나요?
```python
   차원 축소 기법은 고차원 데이터의 차원을 줄여 데이터 분석을 용이하게 하고, 계산 효율성을 높이는 데 사용된다.
   데이터의 특성 (feature) 수를 줄임으로써 과적합을 방지하고, 해석 가능성을 높이며, 계산 비용을 줄일 수 있다.

   ⭐️ PCA (주성분 분석) : 데이터의 분산을 최대한 보존하는 방향으로 새로운 축을 생성하여 고차원 데이터를 저차원으로 변환하는 선형 차원 축소 기법
      - 데이터의 공분산 구조를 분석하여 주성분을 생성한다
      - 첫 번째 주성분은 데이터의 분산이 가장 큰 방향을 나타내며, 그 다음 주성분은 직교하는 방향에서 두 번째로 큰 분산을 나타낸다
      - https://m.blog.naver.com/angryking/222480031842 여기 참고하면 단 번에 이해 가능!
   
```
- PCA는 차원 축소 기법이면서, 데이터 압축 기법이기도 하고, 노이즈 제거기법이기도 합니다. 왜 그런지 설명해주실 수 있나요?
```python
   차원 축소 기법은 위에서 설명
   PCA는 고차원 데이터를 적은 수의 차원으로 압축하면서도 대부분의 중요한 정보를 보존하기에 데이터 압축 기법이라고도 한다
   PCA는 결국 데이터를 분산이 큰 방향으로 투영하기 때문에, 노이즈와 같은 작은 변동을 무시하는 효과가 있다!
```
- LSA, LDA, SVD 등의 약자들이 어떤 뜻이고 서로 어떤 관계를 가지는지 설명할 수 있나요?
```python
   LSA (Latent Semantic Analysis) : 잠재 의미 분석, LSA는 문서와 단어 사이의 관계를 분석하여 텍스트 데이터를 저차원 의미 공간에 매핑하는 기법, 이 과정으로 문서와 단어간의 잠재적 의미 구조 발견
   주로 SVD를 사용하여 문서-단어 행렬을 분해하고 차원을 축소
   LDA (Latent Dirichlet Allocation) : 텍스트 코퍼스 내의 문서들이 잠재적인 주제들의 혼합으로 구성되어 있다고 가정하는 주제 모델링 기법이다. 문서 내의 단어 분포를 기반으로 주제를 추론하고,
   문서들이 어떤 주제들로 구성되어 있는지를 학습한다. 확률적 모델을 사용하여 문서와 단어의 주제 분포를 추정한다.
   SVD (Singular Value Decomposition) : 특이값 분해, 행렬을 세 개의 행렬로 분해하는 선형대수적 기법. 주어진 행렬을 U(왼쪽 특이벡터), Σ(특이값 대각 행렬), V^T(오른쪽 특이벡터)의 곱으로 분해한다!
```
- Markov Chain을 고등학생에게 설명하려면 어떤 방식이 제일 좋을까요?
```python
   일상적인 예시로 시작해서 개념을 단계별로 확장하는 것이 좋다.
   예를 들어, 오늘이 맑음이면 내일도 맑음일 가능성이 높지만, 비가 올 가능성도 있다. 날씨는 현재 상태에 따라 다음 상태가 결정되지만, 그 이전 날들의 날씨는 고려하지 않는다고 가정해 볼 수 있다.
   여기서 중요한 점은 현재 상태만으로 다음 상태가 결정된다는 것이며, 이를 Markov Preperty(마르코프 성질)라고 한다.
   이렇게 상태(state)가 현재 상황에만 의존해서 바뀌는 과정을 바로 Markov Chain이라고 한다!
```
- 텍스트 더미에서 주제를 추출해야 합니다. 어떤 방식으로 접근해 나가시겠나요?
- SVM은 왜 반대로 차원을 확장시키는 방식으로 동작할까요? SVM은 왜 좋을까요?
- 다른 좋은 머신 러닝 대비, 오래된 기법인 나이브 베이즈(naive bayes)의 장점을 옹호해보세요.
- 회귀 / 분류시 알맞은 metric은 무엇일까?
- Association Rule의 Support, Confidence, Lift에 대해 설명해주세요.
- 최적화 기법중 Newton’s Method와 Gradient Descent 방법에 대해 알고 있나요?
- 머신러닝(machine)적 접근방법과 통계(statistics)적 접근방법의 둘간에 차이에 대한 견해가 있나요?
- 인공신경망(deep learning이전의 전통적인)이 가지는 일반적인 문제점은 무엇일까요?
- 지금 나오고 있는 deep learning 계열의 혁신의 근간은 무엇이라고 생각하시나요?
- ROC 커브에 대해 설명해주실 수 있으신가요?
- 여러분이 서버를 100대 가지고 있습니다. 이때 인공신경망보다 Random Forest를 써야하는 이유는 뭘까요?
- K-means의 대표적 의미론적 단점은 무엇인가요? (계산량 많다는것 말고)
- L1, L2 정규화에 대해 설명해주세요.
- Cross Validation은 무엇이고 어떻게 해야하나요?
- XGBoost을 아시나요? 왜 이 모델이 캐글에서 유명할까요?
- 앙상블 방법엔 어떤 것들이 있나요?
- feature vector란 무엇일까요?
- 좋은 모델의 정의는 무엇일까요?
- 50개의 작은 의사결정 나무는 큰 의사결정 나무보다 괜찮을까요? 왜 그렇게 생각하나요?
- 스팸 필터에 로지스틱 리그레션을 많이 사용하는 이유는 무엇일까요?
- OLS(ordinary least squre) regression의 공식은 무엇인가요?

</details>

<details>
<summary><a href="./answers/3-deep-learning.md"><strong>🧠 딥러닝</strong></a></summary>

- 딥러닝은 무엇인가요? 딥러닝과 머신러닝의 차이는?
- Cost Function과 Activation Function은 무엇인가요?
- Tensorflow, PyTorch 특징과 차이가 뭘까요?
- Data Normalization은 무엇이고 왜 필요한가요?
- 알고있는 Activation Function에 대해 알려주세요. (Sigmoid, ReLU, LeakyReLU, Tanh 등)
- 오버피팅일 경우 어떻게 대처해야 할까요?
- 하이퍼 파라미터는 무엇인가요?
- Weight Initialization 방법에 대해 말해주세요. 그리고 무엇을 많이 사용하나요?
- 볼츠만 머신은 무엇인가요?
- TF, PyTorch 등을 사용할 때 디버깅 노하우는?
- 뉴럴넷의 가장 큰 단점은 무엇인가? 이를 위해 나온 One-Shot Learning은 무엇인가?
- 요즘 Sigmoid 보다 ReLU를 많이 쓰는데 그 이유는?
  - Non-Linearity라는 말의 의미와 그 필요성은?
  - ReLU로 어떻게 곡선 함수를 근사하나?
  - ReLU의 문제점은?
  - Bias는 왜 있는걸까?
- Gradient Descent에 대해서 쉽게 설명한다면?
  - 왜 꼭 Gradient를 써야 할까? 그 그래프에서 가로축과 세로축 각각은 무엇인가? 실제 상황에서는 그 그래프가 어떻게 그려질까?
  - GD 중에 때때로 Loss가 증가하는 이유는?
  - Back Propagation에 대해서 쉽게 설명 한다면?
- Local Minima 문제에도 불구하고 딥러닝이 잘 되는 이유는?
  - GD가 Local Minima 문제를 피하는 방법은?
  - 찾은 해가 Global Minimum인지 아닌지 알 수 있는 방법은?
- Training 세트와 Test 세트를 분리하는 이유는?
  - Validation 세트가 따로 있는 이유는?
  - Test 세트가 오염되었다는 말의 뜻은?
  - Regularization이란 무엇인가?
- Batch Normalization의 효과는?
  - Dropout의 효과는?
  - BN 적용해서 학습 이후 실제 사용시에 주의할 점은? 코드로는?
  - GAN에서 Generator 쪽에도 BN을 적용해도 될까?
- SGD, RMSprop, Adam에 대해서 아는대로 설명한다면?
  - SGD에서 Stochastic의 의미는?
  - 미니배치를 작게 할때의 장단점은?
  - 모멘텀의 수식을 적어 본다면?
- 간단한 MNIST 분류기를 MLP+CPU 버전으로 numpy로 만든다면 몇줄일까?
  - 어느 정도 돌아가는 녀석을 작성하기까지 몇시간 정도 걸릴까?
  - Back Propagation은 몇줄인가?
  - CNN으로 바꾼다면 얼마나 추가될까?
- 간단한 MNIST 분류기를 TF, PyTorch 등으로 작성하는데 몇시간이 필요한가?
  - CNN이 아닌 MLP로 해도 잘 될까?
  - 마지막 레이어 부분에 대해서 설명 한다면?
  - 학습은 BCE loss로 하되 상황을 MSE loss로 보고 싶다면?
- 딥러닝할 때 GPU를 쓰면 좋은 이유는?
  - GPU를 두개 다 쓰고 싶다. 방법은?
  - 학습시 필요한 GPU 메모리는 어떻게 계산하는가?

</details>


<details>
<summary><a href="./answers/5-network.md"><strong>🌐 네트워크</strong></a></summary>

- TCP/IP의 각 계층을 설명해주세요.
- OSI 7계층와 TCP/IP 계층의 차이를 설명해주세요.
- Frame, Packet, Segment, Datagram을 비교해주세요.
- TCP와 UDP의 차이를 설명해주세요.
- TCP와 UDP의 헤더를 비교해주세요.
- TCP의 3-way-handshake와 4-way-handshake를 비교 설명해주세요.
- TCP의 연결 설정 과정(3단계)과 연결 종료 과정(4단계)이 단계가 차이나는 이유가 무엇인가요?
- 만약 Server에서 FIN 플래그를 전송하기 전에 전송한 패킷이 Routing 지연이나 패킷 유실로 인한 재전송 등으로 인해 FIN 패킷보다 늦게 도착하는 상황이 발생하면 어떻게 될까요?
- 초기 Sequence Number인 ISN을 0부터 시작하지 않고 난수를 생성해서 설정하는 이유가 무엇인가요?
- HTTP와 HTTPS에 대해서 설명하고 차이점에 대해 설명해주세요.
- HTTP 요청/응답 헤더의 구조를 설명해주세요.
- HTTP와 HTTPS 동작 과정을 비교해주세요.
- CORS가 무엇인가요?
- HTTP GET과 POST 메서드를 비교/설명해주세요.
- 쿠키(Cookie)와 세션(Session)을 설명해주세요.
- DNS가 무엇인가요?
- REST와 RESTful의 개념을 설명하고 차이를 말해주세요.
- 소켓(Socket)이 무엇인가요? 자신 있는 언어로 간단히 소켓 생성 예시를 보여주세요.
- Socket.io와 WebSocket의 차이를 설명해주세요.
- IPv4와 IPv6 차이를 설명해주세요.
- MAC Address가 무엇인가요?
- 라우터와 스위치, 허브의 차이를 설명해주세요.
- SMTP가 무엇인가요?
- 노트북으로 `www.google.com`에 접속을 했습니다. 요청을 보내고 받기까지의 과정을 자세히 설명해주세요.
- 여러 네트워크 topology에 대해 간단히 소개해주세요.
- subnet mask에 대해서 설명해주세요.
- data encapsulation이 무엇인가요?
- DHCP를 설명해주세요.
- routing protocol을 몇 가지 설명해주세요. (ex. link state, distance vector)
- 이더넷(ethernet)이 무엇인가요?
- client와 server의 차이점을 설명해주세요.
- delay, timing(jitter), throughput 차이를 설명해주세요.

</details>

<details>
<summary><a href="./answers/6-operating-system.md"><strong>🖥️ 운영체제</strong></a></summary>

- 프로세스와 스레드의 차이(Process vs Thread)를 알려주세요.
- 멀티 프로세스 대신 멀티 스레드를 사용하는 이유를 설명해주세요.
- 캐시의 지역성에 대해 설명해주세요.
- Thread-safe에 대해 설명해주세요. (hint: critical section)
- 뮤텍스와 세마포어의 차이를 설명해주세요.
- 스케줄러가 무엇이고, 단기/중기/장기로 나누는 기준에 대해 설명해주세요.
- CPU 스케줄러인 FCFS, SJF, SRTF, Priority Scheduling, RR에 대해 간략히 설명해주세요.
- 동기와 비동기의 차이를 설명해주세요.
- 메모리 관리 전략에는 무엇이 있는지 간략히 설명해주세요.
- 가상 메모리에 대해 설명해주세요.
- 교착상태(데드락, Deadlock)의 개념과 조건을 설명해주세요.
- 사용자 수준 스레드와 커널 수준 스레드의 차이를 설명해주세요.
- 외부 단편화와 내부 단편화에 대해 설명해주세요.
- Context Switching이 무엇인지 설명하고 과정을 나열해주세요.
- Swapping에 대해 설명해주세요.

</details>

<details>
<summary><a href="./answers/7-data-structure.md"><strong>🗂 자료구조</strong></a></summary>

- linked list
  - single linked list
  - double linked list
  - circular linked list
- hash table
- stack
- queue
  - circular queue
- graph
- tree
  - binary tree
  - full binary tree
  - complete binary tree
  - bst(binary search tree)
- heap(binary heap)
  - min heap
  - max heap
- <b>RedBlack Tree</b> 🌲
  ```python
    Red-Black Tree는 이진 탐색 트리의 일종으로,
    삽입 및 삭제 시 트리의 균형을 유지하기 위해 각 노드를 빨간색 또는 검은색으로 색칠하여, 특정 규칙을 따라 높이가 균형 잡히도록 보장하는 트리입니다.
    1. 모든 노드는 빨간색 혹은 검은색이어야 합니다.
    2. 루트 노드는 검은색이다.
    3. 모든 NIL은 검은색이다. (NIL : null leaf, 자료를 갖지 않고 트리의 끝을 나타내는 리프 노드)
    4. 빨간색 노드의 자식은 반드시 검은색이다.
    5. NIL에서 루트 노드까지 가는 경로에서 만나는 검은색 노드의 개수가 같다.
  ```
- b+ tree

</details>

<details>
<summary><a href="./answers/8-algorithm.md"><strong>🔻 알고리즘</strong></a></summary>

- 시간, 공간 복잡도
- Sort Algorithm
  - Bubble Sort
  ```python
    인접한 두 요소를 비교하여 큰 값을 뒤로 보내는 방식으로 배열을 정렬한다.
    복잡도: O(n^2)
    특징: 구현이 간단하지만 효율성이 떨어져 잘 사용하지 x
  ```
  - Selection Sort
  ```python
     매번 배열에서 가장 작은 요소를 선택해 순서대로 배치한다.
     복잡도: O(n^2)
     특징: 간단하지만 대규모 데이터에서는 비효율적
  ```
  - Insertion Sort
  ```python
     배열의 요소를 하나씩 가져와서 정렬된 부분에 삽입하는 방식으로 정렬
     복잡도: O(n^2)
     특징: 거의 정렬된 배열에서는 효율적이며, 적은 데이터에 적합하다
  ```
  - Merge Sort O(nlogn) 
  ```python
     배열을 반으로 나누어 각각의 재귀적으로 정렬한 후, 병합하여 전체를 정렬
     복잡도: O(nlogn)
     특징: 안정적이며, 큰 데이터셋에 적합. Divide and Conquer 방식의 알고리즘이다
  ```
  - Heap Sort O(nlogn)
  ```python
     힙 자료구조를 이용하여 정렬하는 방식으로, 최대 힙이나 최소 힙을 이용한다
     복잡도: O(nlogn)
     특징: 제자리 정렬이 가능하지만, 안정적이지는 x
  ```
  - Quick Sort O(nlogn)
  ```python
     기준 요소(pivot)을 정해 이를 기준으로 작은 요소는 왼쪽, 큰 요소는 오른쪽으로 분할하여 재귀적으로 정렬한다
     복잡도: 평균은 O(nlogn), 최악 O(n^2)
     특징: 일반적으로 매우 빠르며, Divide and conquer 알고리즘
  ```
  - Counting Sort
  ```python
     값의 범위가 정해진 배열에서 각 값의 빈도를 세어 정렬한다
     1. 각 숫자가 몇 번 등장하는지 세어준다
     2. 등장 횟수를 누적합으로 바꿔준다
     복잡도: O(n+k)
     특징: 특정 범위에서만 사용 가능하며, 메모리 사용량이 크지만 안정적이다.
  ```
- Divide and Conquer
```python
   분할 정복은 작은 단위로 나누어 해결한 뒤, 이를 합쳐서 전체 문제의 해결책을 도출하는 알고리즘 설계 패턴이다. Divide -> Conquer -> Combine
   예시로는 Merge Sort, Quick sort, Binary Search 
```
- Dynamic Programming
```python
   Dynamic programming은 복잡한 문제를 작은 하위 문제로 나누어 해결하고, 이를 저장하여 중복 계산을 줄이는 방식으로 문제를 효율적으로 해결하는 알고리즘 설계 기법이다. 특히 최적화 문제에서 자주 사용된다!
   Optimal Substructure: 문제의 최적 해결책이 그 하위 문제들의 최적 해결책으로부터 만들어질 수 있는 구조를 말한다
   Overlapping Subproblems: 큰 문제를 작은 문제로 나눌 때 동일한 하위 문제가 여러 번 반복해서 등장한다
   Top-down, Bottom-up 방식으로 해결할 수 있다
   피보나치 수열 예시로 수업 때 설명하심!
```
- Greedy Algorithm
```python
   문제를 해결할 때 각 단계에서 가장 최선의 선택을 하는 방식으로 최종 해답을 찾아가는 알고리즘 설계 방법
   그리디 알고리즘은 전체적인 최적해를 보장하지는 않지만, 일부 문제에서는 빠르고 간단하게 최적해를 구할 수 있는 방법을 제공한다
```
- Graph
  - Graph Traversal: BFS
  ```python
   BFS는 시작 노드에서 인접한 노드들을 먼저 방문하고, 그 다음으로 인접 노드들의 인접 노드들을 차례로 탐색하는 방식이다.
   작동 방식:
   1. 탐색을 시작할 노드를 큐에 추가한다
   2. 큐에서 노드를 하나씩 꺼내어 해당 노드와 연결된 인접 노드들을 큐에 추가한다
   3. 큐가 빌 때까지 이 과정을 반복하며, 방문한 노드는 다시 탐색하지 않는다
   최단 경로: BFS는 최단 경로를 보장한다.
   시간 복잡도 : O(V+E)
  ```
  - Graph Traversal: DFS
  ```python
   DFS는 한 노드에서 시작하여 가능한 깊이까지 내려가며 탐색을 진행하고, 더 이상 갈 곳이 없으면 다시 돌아와 다른 경로를 탐색하는 방식이다.
   작동 방식:
   1. 탐색을 시작할 노드를 스택에 추가한다.
   2. 스택에서 노드를 하나씩 꺼내고, 해당 노드의 인접 노드를 다시 스택에 추가하여 깊이 탐색을 진행한다.
   3. 스택이 빌 때까지 이 과정을 반복하며, 방문한 노드는 다시 탐색하지 않는다.
   경로 탐색: DFS는 특정 경로를 탐색하거나, 특정 상태에 도달했을 때의 조건을 검사하는 데 유용하다.
   시간 복잡도 : O(V+E)
   스택을 사용하여 재귀 호출을 진행하여, 최대 깊이만큼 메모리 필요!
  ```
  - Shortest Path
    - Dijkstra
    ```python
      다익스트라 알고리즘은 가중치가 있는 그래프에서 하나의 시작 정점으로부터 다른 모든 정점까지의 최단 경로를 찾는 알고리즘이다.
      1. 초기화
       - 모든 정점에 대해 시작 정점으로부터의 최단 거리를 무한대로 설정. 시작 정점은 거리를 0으로 설정
       - 방문하지 않은 정점들의 집합인 우선순위 큐를 생성한다
      2. 정점 선택
       - 현재 방문하지 않은 정점들 중에서 시작 정점으로부터의 거리가 가장 짧은 정점을 선택한다
      3. 거리 업데이트
       - 선택된 정점의 인접한 이웃 정점들을 확인한다
       - 각 인접 정점에 대해, 시작 정점으로부터 현재 정점을 거쳐서 이웃 정점으로 가는 경로의 거리를 계산한다
       - 계산된 거리가 현재 저장된 시작 정점으로부터 이웃 정점까지의 거리보다 작으면, 해당 거리를 업데이트한다
      4. 방문 완료 처리
       - 선택된 정점을 방문 처리하고 우선순위 큐에서 제거한다
       - 모든 정점을 방문할 때까지 2~4단계를 반복한다!
    ```
    - Floyd-Warshall
    ```python
      Floyd Warshall은 모든 정점 쌍 간의 최단 경로를 찾는 알고리즘으로, 동적 계획법을 사용하여 그래프의 최단 경로 문제를 해결한다.
      이 알고리즘은 특히 음수 가중치를 가진 간선을 포함한 그래프에서도 최단 경로를 찾을 수 있으며, 음수 사이클도 감지할 수 있다.
    ```
    - Bellman-Ford
    ```python
      벨만 포드 알고리즘은 하나의 시작 정점에서 모든 다른 정점까지의 최단 경로를 찾는 알고리즘으로, 특히 음수 가중치 간선이 포함된 그래프에도 최단 경로를 구할 수 있는 특징이 있다.
      벨만 포드 알고리즘은 모든 간선을 최대 V-1번 반복하여 최단 경로를 갱신해 나간다. 이때 V는 정점의 개수이다.
    ```
  - Minimum Spanning Tree
    - Prim
    ```python
      Prim 알고리즘은 최소 신장 트리 (MST)를 찾기 위한 알고리즘으로, 정점 중심 방식으로 트리를 점진적으로 확장해 가며 MST를 구축하는 방식이다.
      MST는 모든 정점을 포함하면서 간선의 가중치 합이 최소가 되는 트리를 의미한다.
      1. 시작 정점 선택 : 임의의 시작 정점을 선택하여 초기 트리를 시작한다
      2. 가장 작은 가중치의 간선 선택 : 트리에 포함된 정점에서 연결된 간선 중 가중치가 가장 작은 간선을 선택한다. 이 간선의 도착 정점을 트리에 추가하여 트리를 확장한다.
      3. 트리의 확장: 현재의 MST에 포함된 정점 집합과 연결된 간선 중에서 가장 작은 가중치를 가진 간선을 선택하여 트리에 추가한다.
      4. 반복: 모든 정점을 포함할 때까지 즉 MST가 완성될 때까지 2~3 단계를 반복한다. 
    ```
    - Kruskal
    ```python
      Kruskal 알고리즘은 그래프에서 최소 신장 트리를 찾기 위한 알고리즘이다. 이 알고리즘은 간선 중심으로 동작하며, 모든 간선을 가중치 순으로 정렬한 후, 사이클을 형성하지 않는 간선을 하나씩 추가하여 MST를 구성하는 방식이다.
      1. 간선 정렬: 그래프의 모든 간선을 가중치의 오름차순으로 정렬한다
      2. 간선 선택 및 사이클 검증 : 가중치가 가장 작은 간선부터 하나씩 선택하여, 사이클이 발생하지 않는 경우에만 MST에 추가한다.
         2-1. 사이클이 발생하는지 확인하기 위해 Union-Find 자료구조를 사용한다.
              - Find 연산 : 두 정점이 같은 집합에 속하는지 확인한다.
              - Union 연산 : 두 정점을 같은 집합으로 병합하여, 동일한 트리로 연결되었음을 표시한다.
      3. 반복: 간선을 추가하여 MST에 포함된 간선의 수가 (정점 수 - 1)이 될 때까지 반복한다.
              - MST는 연결 그래프이므로 간선의 수는 정점 수 - 1이 된다.
    ```
  - Union-find
  ```python
      Union Find는 서로소 집합을 관리하는 자료구조이다. 서로소 집합 자료구소는 여러 개의 집합을 효율적으로 관리하고, 각 원소가 어느 집합에 속하는지 확인하거나, 두 집합을 하나로 합치는 연산을 빠르게 수행할 수 있도록 설계되었다.
      Union-Find 자료구조는 그래프에서의 사이클 검출, 최소 신장 트리 구성(Kruskal 알고리즘) 등 다양한 알고리즘에서 활용된다.
  ```
  - Topological sort 위상정렬
  ```python
     위상정렬은 유향 비순환 그래프 DAG(Directed Acyclic Graph)에서 정점들을 선행 순서에 맞춰 정렬하는 방법이다. DAG는 순환이 없는 방향 그래프로, 위상 정렬은 주로 작업 간의 우선 순위가 있는 작업 스케줄링 등에서 사용된다.
     위상 정렬은 다음과 같은 조건을 만족하는 정렬 방식이다.
     - 정점 u에서 v로 가는 간선이 존재한다면, 정렬 결과에서 u는 항상 v보다 앞에 위치해야 한다
     위상 정렬은 두 가지 방식으로 구현할 수 있다.
     - Kahn's Algorithm (BFS 기반)
     - DFS 기반 방법
  ```
</details>

---
