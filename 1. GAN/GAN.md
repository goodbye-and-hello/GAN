## 1. GAN - Generative Adversarial Networks

**Generative Adversarial Networks** (이하 GAN) 은 2014년도에 *Ian Goodfellow*에 의해 제안되었다. 

두개의 Neural Network가 서로 경쟁 또는 다른 관점에서 바라보면 두 Neural Network가 공동으로

작업을 한다.



한 Neural Network는 실제 데이터와 가까운 데이터를 생성하려고 하고 또 다른 Neural Network는

이전의 Neural Network에서 생성된 데이터와 실제 데이터를 구별 하려고 시도합니다.

GAN은 모든 데이터 분포를 모델링 할 수 있지만 최근에는 주로 이미지 데이터에 주로 사용됩니다.

각각의 Neural Network를 NN1 과 NN2로 표기하겠습니다.



NN1은 Loss Function으로 **Discriminator**를 사용하고 매개변수를 업데이트하여 현실감있게 보이는 데이터를 생성합니다.



![](https://github.com/ssibongee/GAN/blob/master/1.%20GAN/GANs.png?raw=true)



반면 NN2는 매개변수를 업데이트하여 실제 데이터에서 가짜 데이터를 잘 구별하기 위해 매개변수를 업데이트 합니다.  



여기서 NN1은 무작위로 추측할 수 있을 만큼 실제처럼 보이는 데이터를 생성합니다. 위의 ***Game of Cat and Mouse***은 소위 말하는 *equilibrium* 에 도달할 때까지 계속 반복하게 됩니다.



즉, 간단히 GAN을 간단히 표현하자면 데이터를 생성하는 Neural Network와 다른 하나는 가짜 데이터와 실제 데이터를 분류하는 Neural Network를 서로 경쟁하여 NN1이 완전히 새롭고 현실적인 데이터를 생성할 수 있는 지점까지 훈련을 반복하는 것이다.