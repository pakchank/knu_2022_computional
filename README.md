# 1. Introduction

## Motivational Example: Logit Models

확률, 최적화, 수학의 추정에서의 유용성을 이해하기 위해서 다음과 같은 예를 생각해 보자.&#x20;

각 응답자는 어떤 뉴스 서비스를 구독할지를 결정해야 한다. 우리가 이 결정을 이해하기 위해서 세울 수 있는 하나의 모형(model)은 응답자가 뉴스 서비스를 구독할 때 느끼는 효용($$U_A$$)과 구독하지 않을 때 느끼는 효용($$U_B$$)을 비교한다고 생각하는 것이다. 더 나아가, 각각의 효용은 나이($$x_i$$​)와 가격($$p_j$$​), 그리고 관찰할 수 없는 어떤 요인($$\epsilon_{iA}$$,$$\epsilon_{iB}$$)에 의해 결정된다고 생각해 보자. 즉,

$$
U_{Ai}=\beta_{0A} + \beta_{1A} x_i + \beta_{2A} p + \epsilon_{iA}
$$

$$
U_{Bi} = \beta_{0B} + \beta_{1B} x_i + \beta_{2B} 0 + \epsilon_{iB}
$$

​그렇다면, 이 이용자는 $$U_{Ai} \geq U_{Bi}$$​일때 해당 서비스에 구독하게 될 것이다. 그러나 관측불가능한 요인들이 있으므로, 구독 결정은 확률로만 표현할 수 있다.

​



&#x20;

1. 마치 parameter를 안다고 생각하고 behavioral model을 생각할 것이다 (population model)
2. Estimation을 위한 cost function 또는 max/min할 function을 만든다.
3. 이제 미지의 parameter를 maximize한다.&#x20;



* RUM model (EC 823에서 했던 대로) -> 모델을 만든다 (마치 parameter를 아는 것처럼) + probability -> 이건 적분의 영역.
* 그 다음에 liklihood는 Bernouille로 가지 말고 Coursera에서 했던 대로... -> 이건 미분의 영역. &#x20;
