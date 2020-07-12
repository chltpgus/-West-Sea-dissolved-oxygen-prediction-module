# West-Sea-dissolved-oxygen-prediction-module (서해 용존산소량 예측 모듈)

# 작품 소개
jupyter를 이용해서 서해 바다 CSV파일을 분석하고 서해 용존산소량을 예측하는 모듈을 제작하였다.

# 작품 설명 
![image](https://user-images.githubusercontent.com/67909892/87246406-3448bd00-c488-11ea-803f-567be8f9b139.png)

CSV파일에에 화학 산소 요구량을 이진 분리하기(class) 위해 화학 산소 요구량 > 2.5 이면 1을 주고, 화학 산소 요구량 <=2.5 이면 0을 주는 I 열을 추가하였다.

![image](https://user-images.githubusercontent.com/67909892/87246422-622e0180-c488-11ea-93b5-15c626efa053.png)

용존산소량에 따른 class 값을 확인 할 수 있다. 자료를 통해 용존 산소량이 높을수록 class가 1에 가깝고 낮을수록 0에 가까운 것이 확인되었다.

![image](https://user-images.githubusercontent.com/67909892/87246427-75d96800-c488-11ea-8cf4-60e1bf73e875.png)

heatmap을 통해서 자료들을 시각화하였다.

![image](https://user-images.githubusercontent.com/67909892/87246439-8ab5fb80-c488-11ea-8532-1915db90c541.png)

tensorflow와 keras를 이용해서 Sequential, Dens를 import 해주고 Seed 값을 생성해준 후 CSV파일을 열어 input, output 데이터를 설정해준다.

![image](https://user-images.githubusercontent.com/67909892/87246452-9acddb00-c488-11ea-8a18-f08b718e87f7.png)

다음으로 모델을 설정해준다. 데이터가 8개가 들어가기 때문에 은닉층 input_dim을 8로 해주고 활성함수를 relu를 사용해서 모델을 설정한다. 출력층의 활성함수를 sigmoid로 설정을 끝내준다.
그리고 모델을 컴파일한다.

![image](https://user-images.githubusercontent.com/67909892/87246470-acaf7e00-c488-11ea-8f88-9462a7dbfc95.png)

모델을 실행한다. 100번을 실행해 모듈을 학습한다. accuracy : 의 숫자가 학습을 통해서 점점 정확도가 올라가는 것이 확인된다.

![image](https://user-images.githubusercontent.com/67909892/87246484-bc2ec700-c488-11ea-8ab0-4537747c5749.png)

학습한 모듈로 결과를 출력한다. 99퍼센트에 가까운 값이 나온다. 99퍼센트의 효율을 내는 용존산소량 예측 모듈을 만들었다.
