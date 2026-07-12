# [Expectation–maximization algorithm](https://en.wikipedia.org/wiki/Expectation%E2%80%93maximization_algorithm)

통계에서, expectation-maximization (EM) 알고리즘은 관측되지 않은 잠재 변수에 의존하는 통계 모델에서 파라미터의 로컬 maximum likelihood 또는 maximum a posteriori 추정치를 찾기위한 반복적 방법이다. <br>
EM 알고리즘은 E 단계(현재의 파라미터로부터 log-likelihood 기댓값을 나타내는 함수를 만드는 단계)와 M 단계 (E 단계에서 계산된 기대 log-likelihood값을 최대화하는 파라미터를 구하는 단계)를 반복한다. <br>
파라미터 추정치는 다음 E 단계의 잠재 변수의 분포를 결정하는데 사용된다.<br>
예를 들어, Mixture of Gaussian을 추정하거나 다항 선형 회귀 문제를 푸는데 사용할 수 있다.<br>

## Introduction

EM 알고리즘은 한 번에 풀 수 없는 방정식을 가진 통계 모델에서 파라미터의 지역 maximum likelihood를 찾는데 사용된다. <br>
일반적으로 이러한 모델은 잠재변수와 더불어 알려지지 않은 파라미터와 데이터로부터 관측된 파라미터를 포함한다.<br>
즉, 결측값이 데이터 사이에 존재하거나, 관측되지 않은 데이터 포인터의 존재를 가정함으로써 모델의 공식을 단순화할 수 있다.

예를 들어, mixture 모델은 각 관측된 데이터 포인트가 관측되지 않은 데이터 포인터에 대응되거나 각 데이터 포인터에 속한다고 지정된 잠재변수에 대응됨을 가정함으로써 더 간단하게 묘사할 수 있다. <br>

maximum likelhood 풀이를 찾는 것은 일반적으로 모든 미지수(파라미터와 잠재변수)에 대한 likelihood 함수의 도함수를 구하는 과정이 필요로하고, 동시에 결과의 방정식을 푸는 것이 필요로 한다.


- in addition to: ~에 더하여, ~뿐만 아니라

> That is, either missing values exist among the data, or the model can be formulated more simply by assuming the existence of further unobserved data points.

- either A or B: A 이거나 B 이거나
- derivatives : 도함수, 편미분값
- equations: 방정식

>  For example, a mixture model can be described more simply by assuming that each observed data point has a corresponding unobserved data point, or latent variable, specifying the mixture component to which each data point belongs.

- an unobserved variable, or a latent variable, -> an unobserved variale (a latent variable)

> Finding a maximum likelihood solution typically requires taking the derivatives of the likelihood function with respect to all the unknown values, the parameters and the latent variables, and simultaneously solving the resulting equations.

-  all the unknown values, the parameters and the latent variables ->  all the unknown values(the parameters and the latent variables)
