# 가로등 매니저 (ICT 융합 프로젝트)

<br>
<br>
<br>
<br>

## 작품 개요
 밤에 길을 걷다 보면 종종 고장 난 가로등이 보일 때가 많이 있다. 특히 시골이나 달동네 같은 곳은 가로등이 고장 나게 되면 야간에 아무것도 보이지 않는다. 그리고 어둡고 아무도 볼 수 없다는 이유로 범죄의 위험성을 매우 높일 수 있다고 한다.
 
 우리는 처음 이런 가로등의 관리가 어떻게 이뤄지는지 궁금했고 알아본 결과 시민들의 고장 신고 전화 외에 가로등이 고장이 났는지 정상 작동하는지 알 수 있는 경우가 없다는 것을 알게 되었다. 그래서 우리가 배운 지식을 통해 고장 난 가로등을 효율적으로 관리하는 방법을 생각해 보게 되었다.
 
 가로등에 센서를 달고 센서값을 서버에서 확인하여 가로등의 고장 유무를 상황실 내에서 알 수 있게 함으로써 좀 더 체계적인 관리가 이루어질 수 있도록 만들어 보았다.
<br>
<br>
<br>
<br>

## 작품 설명
 가로등에 조도 센서를 포함한 아두이노 모듈을 설치하고, 일정 시간마다 측정된 평균치 및 가로등 고유번호를 와이파이 통신을 이용하여 서버로 전송한다.

 서버에서는 측정치를 전송받아 일정 기준치 ( 우리가 실내 실외에서 실험한 기준치 값은 700이다.)를 벗어나면 고장임을 인식한다. 이상이 있는 값을 보낸 가로등 고유번호 및 제어 신호(LED ON/OFF signal)를 아두이노 모듈이 연결된 상황판에 시리얼 통신을 이용해 전송한다.
 
 상황판에서 전송받은 가로등 번호에 해당하는 LED를 찾아 같이 전송받은 제어 신호에 해당하는 동작(LED ON/OFF)을 한다. 
서버실에서는 상황판을 보고 고장 난 가로등을 식별하여 조치한다.
<br>
<br>
<br>
<br>

### Prerequisites / 선행 조건

아래 사항이 되어있어야합니다.

```
프로젝트를 진행하기 위해 아두이노 우노, 조도센서, LED 센서, wifi 모듈, 후레쉬가 필요합니다.
```
<br>
<br>
<br>
<br>

### Installing / 설치

아래 개발 환경이 설정 되어 있어야 실행할 수 있습니다.

```
arduino, atom IDE를 통해 개발을 진행했습니다.
```
<br>
<br>
<br>
<br>

## Running the tests / 테스트의 실행

![image](https://user-images.githubusercontent.com/51222715/119217931-8af73c80-bb18-11eb-8edd-b8329e246183.png)
<br>

1. 가로드 매니저 회로도입니다. 해당 제품을 통해 빛을 감지하고 WiFi 모듈을 통해 서버로 데이터를 전송합니다.

![image](https://user-images.githubusercontent.com/51222715/119217951-a9f5ce80-bb18-11eb-9e24-a3b77b880011.png)
<br>

2. 상황판을 만들어 가로등 매니저 갯수(3개)에 맞춰 만약 문제가 생기면 LED등에 불빛이 들어오게 설계했습니다.

<br>
<br>
<br>
<br>

### 테스트는 이런 식으로 작성하시면 됩니다

```
실제 테스트를 한 환경은 최종 보고서 파일을 보고 확인하시면 됩니다.
```

