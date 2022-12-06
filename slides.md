---
theme: purplin
layout: intro
---

# Serverless right now!

서버리스 아키텍쳐가 낯설다면 망설이지 말GO!

### seongspa

---
layout: intro
---

## 소개 말씀

<br />
<br />

안녕하세요. `seongspa` 입니다.

42 Seoul `m_htkim` 멘토님의 Cloud: design and process 강의를 듣고 소프트웨어 아키텍쳐에 관심을 가지게 되었습니다.

AWS x 42 Adelaide에서 주관한  Cloud Quest에서 Seoul 리젼 1등을 했습니다.

디지털유목민이 되고 싶은데요.

어찌보면 한 곳에 거처를 두지않고 돌아다닌다는 점에서 서버리스 아키텍쳐와 저는 떼려야  뗄 수 없을 것 같네요.



<BarBottom  title="Serverless right now!">
  <Item text="seongs1024/serverless-right-now">
    <carbon:logo-github />
  </Item>
  <Item text="seongspa">
    <img
      src="https://42.fr/wp-content/uploads/2021/05/42-Final-sigle-seul.svg"
      class="w-5"
    />
  </Item>
</BarBottom>

---
layout: intro
---

## 나누고 싶은 이야기

<br />
<br />

Part 1. Serverless XO, 서버리스에대해 알아가는 시간!

Part 2. Hands-on labs, 서버리스 컴퓨팅의 핵심 요소인 AWS Lambda를 사용해봐요!

Part 3. Ask me anything, 서버리스에 대해서 무엇이든 물어보세요!

<BarBottom  title="Serverless right now!">
  <Item text="seongs1024/serverless-right-now">
    <carbon:logo-github />
  </Item>
  <Item text="seongspa">
    <img
      src="https://42.fr/wp-content/uploads/2021/05/42-Final-sigle-seul.svg"
      class="w-5"
    />
  </Item>
</BarBottom>

---
layout: intro
---

## 누가 들으면 좋을까요?

<br />
<br />

서버리스 초보자👶, 클라우드 입문자, 그리고 클라우드에 관심있는 사람이라면 누구나 대상으로 합니다.

서비스 기획단계에서 서버리스 아키텍쳐를 검토하고 계신 분들께 도움이 될 수도(?) 있습니다.

숙련자분께는 내용이 뻔할 수 있어 뒤쪽에 다과를 섭취하면서 저를 귀엽게 봐주셨으면 합니다. (디펜스 환영!)

감사합니다.

<BarBottom  title="Serverless right now!">
  <Item text="seongs1024/serverless-right-now">
    <carbon:logo-github />
  </Item>
  <Item text="seongspa">
    <img
      src="https://42.fr/wp-content/uploads/2021/05/42-Final-sigle-seul.svg"
      class="w-5"
    />
  </Item>
</BarBottom>

---
layout: intro
---

# Part 1. Serverless XO

---
layout: intro
---

## 들어가기에 앞서 클라우드 서비스는 어떻게 사용하고 계신가요?

<br />
<br />

서버를 온프레미스로 구현하셨다고요?

클라우드 서비스 이용하신다고요?

서버가 없다고요?

아니 서버가 없을 수가 있나요?

이와 관련해서 궁금증이 있는 어떤 사람을 소개시켜드릴게요.

<BarBottom  title="Serverless right now!">
  <Item text="seongs1024/serverless-right-now">
    <carbon:logo-github />
  </Item>
  <Item text="seongspa">
    <img
      src="https://42.fr/wp-content/uploads/2021/05/42-Final-sigle-seul.svg"
      class="w-5"
    />
  </Item>
</BarBottom>

---
layout: image-x
image: ./figures/stick-in-cap.png
imageOrder: 1
---

하이, 나 아기 카뎃.

번뜩이는 사이드 프로젝트 하나 가져왔어.

바로, 42 슐랭이야.

클러스터 주변 맛집 지도 제작해보려고!

잘 부탁해.

<BarBottom  title="Serverless right now!">
  <Item text="seongs1024/serverless-right-now">
    <carbon:logo-github />
  </Item>
  <Item text="seongspa">
    <img
      src="https://42.fr/wp-content/uploads/2021/05/42-Final-sigle-seul.svg"
      class="w-5"
    />
  </Item>
</BarBottom>

---
layout: image-x
image: ./figures/frontend.png
imageOrder: 1
---

오케이, 비지니스 로직 간단하고 👌

프론트는 Node.js, React, JS, CSS, HTML이면

사이트 뚝딱이겠네 ㅎㅎ 

<BarBottom  title="Serverless right now!">
  <Item text="seongs1024/serverless-right-now">
    <carbon:logo-github />
  </Item>
  <Item text="seongspa">
    <img
      src="https://42.fr/wp-content/uploads/2021/05/42-Final-sigle-seul.svg"
      class="w-5"
    />
  </Item>
</BarBottom>

---
layout: image-x
image: ./figures/backend.png
imageOrder: 1
---

갑자기 백엔드 생각하니 골치가 아파졌다.

<BarBottom  title="Serverless right now!">
  <Item text="seongs1024/serverless-right-now">
    <carbon:logo-github />
  </Item>
  <Item text="seongspa">
    <img
      src="https://42.fr/wp-content/uploads/2021/05/42-Final-sigle-seul.svg"
      class="w-5"
    />
  </Item>
</BarBottom>

---
layout: quote
position: center
---

# "서버를 제일 잘 관리하는 방법은
# 서버가 없는 것이다."
-- Werner Vogels, Amazon CTO

<BarBottom  title="Serverless right now!">
  <Item text="seongs1024/serverless-right-now">
    <carbon:logo-github />
  </Item>
  <Item text="seongspa">
    <img
      src="https://42.fr/wp-content/uploads/2021/05/42-Final-sigle-seul.svg"
      class="w-5"
    />
  </Item>
</BarBottom>

---
layout: intro
---

우리가 전달할 솔루션에 물리적인 서버 자체가 포함되어 있나요?

직접 서버를 만들어서 그 위에 모든 걸 구축하고 관리하는 것이 42 슐랭이 제공하고 싶은 비지니스인가요?

그게 아니라면 **필요한 서비스는 제공받으면 되는 것입니다.**

<BarBottom  title="Serverless right now!">
  <Item text="seongs1024/serverless-right-now">
    <carbon:logo-github />
  </Item>
  <Item text="seongspa">
    <img
      src="https://42.fr/wp-content/uploads/2021/05/42-Final-sigle-seul.svg"
      class="w-5"
    />
  </Item>
</BarBottom>

---
layout: intro
---

## *-a-a-S, etc.

: anything as a service

어떤 것을 서비스로 제공받는다는 의미인데 쉽게 말해 대여한다고 생각해보시죠.

|     |     |
| --- | --- |
| <kbd>IaaS</kbd> | 서버, 스토리지, 네트워크 등 인프라를 대여 |
| <kbd>PaaS</kbd> | 개발을 도와주는 플랫폼을 대여 |
| <kbd>SaaS</kbd> | 소프트웨어를 대여 |
| <kbd>BaaS</kbd> <- serverless | 백엔드 기능(데이터베이스, 소셜미디어 연동, 파일시스템 등)을 대여 |
| <kbd>FaaS</kbd> <- serverless | 함수를 대여 |

<BarBottom  title="Serverless right now!">
  <Item text="seongs1024/serverless-right-now">
    <carbon:logo-github />
  </Item>
  <Item text="seongspa">
    <img
      src="https://42.fr/wp-content/uploads/2021/05/42-Final-sigle-seul.svg"
      class="w-5"
    />
  </Item>
</BarBottom>

---
layout: intro
---

## BaaS

<br />
<br />

BaaS는 단일 웹페이지나 모바일 앱 기반의 서비스에서 필요한 백앤드 기능(로그인, 데이터 관리, 회원 관리 등)을 개발자가 직접 개발하지 않고 클라우드 공급자가 제공하는 서비스를 이용해 쉽고 안정적으로 구현하는 것입니다.

애플리케이션에 당연히 요구되지만 구현하기는 번거로운 데이터 저장소, 파일 저장소, SNS 연동, 위치 정보 검색, 푸쉬 알림과 같은 기능을 API 방식으로 제공하기 때문에 필요한 기능을 호출해서 사용할 수 있습니다.

대표적으로 GCP의 Firebase와 AWS의 Amplify 등이 있습니다.

<BarBottom  title="Serverless right now!">
  <Item text="seongs1024/serverless-right-now">
    <carbon:logo-github />
  </Item>
  <Item text="seongspa">
    <img
      src="https://42.fr/wp-content/uploads/2021/05/42-Final-sigle-seul.svg"
      class="w-5"
    />
  </Item>
</BarBottom>

---
layout: intro
---

## FaaS

<br />
<br />

FaaS는 기능을 하나의 함수로 구현해두고 실행할 때마다 서버 자원을 할당받아 사용하는 것을 말합니다.

이벤트 기반의 아키텍처를 구현하는데 적합하며 사용자가 원하는 기능을 미리 작성해놓고 특정 이벤트(예를 들어 HTTP 요청, API 호출, 특정 조건 등)에 의해 실행됩니다. 이때 서버는 대기하면서 이벤트를 기다리지 않고 이벤트가 발생할 때마다 실행됩니다. 비용은 함수가 실행된 횟수와 시간에 따라 산정됩니다.

대표적인 서비스로 AWS의 Lambda, Microsoft Azure의 Functions, GCP의 Cloud Functions 등이 있습니다.

<BarBottom  title="Serverless right now!">
  <Item text="seongs1024/serverless-right-now">
    <carbon:logo-github />
  </Item>
  <Item text="seongspa">
    <img
      src="https://42.fr/wp-content/uploads/2021/05/42-Final-sigle-seul.svg"
      class="w-5"
    />
  </Item>
</BarBottom>

---
layout: intro
---

## 서버리스의 장점

<br />
<br />

- 💵 인보케이션 횟수와 처리 시간에 따라 요금이 부과돼서 요금이 최적화될 거에요. ~~돈이 최고야!~~
- 🎯 비지니스 로직에 더 몰두할 수 있어요.
- 📈 스케일 아웃하기 쉬워요.
- 🔧 관리가 편해요. ~~서버보다 상대적으로~~
- 📦 모듈화하기 좋아요. 마이크로서비스!

<BarBottom  title="Serverless right now!">
  <Item text="seongs1024/serverless-right-now">
    <carbon:logo-github />
  </Item>
  <Item text="seongspa">
    <img
      src="https://42.fr/wp-content/uploads/2021/05/42-Final-sigle-seul.svg"
      class="w-5"
    />
  </Item>
</BarBottom>

---
layout: intro
---

## 서버리스 단점은 없나요?

<br />
<br />

- 콜드스타트
- 타임아웃 <- [장시간 쿼리문 돌리는 법](https://stackoverflow.com/questions/65608892/is-there-a-time-limit-for-running-serverless-batch-job)
- 벤더락인
- 가격 예측 어려움
- 통합테스트 어려움 <- [Hexagonal architecture principles](https://github.com/serverlesspolska/serverless-hexagonal-template)
- (설계 방식의 변화)
- (Stateless) <- [Step functions 등으로 극복 가능](https://docs.aws.amazon.com/step-functions/latest/dg/tutorial-creating-lambda-state-machine.html)

<BarBottom  title="Serverless right now!">
  <Item text="seongs1024/serverless-right-now">
    <carbon:logo-github />
  </Item>
  <Item text="seongspa">
    <img
      src="https://42.fr/wp-content/uploads/2021/05/42-Final-sigle-seul.svg"
      class="w-5"
    />
  </Item>
</BarBottom>

---
layout: intro
---

## 서버리스 사례가 주변에 있나요?

<br />
<br />

<div class="grid grid-cols-2 gap-x-4">
<div>

- 정적 웹페이지
- 챗봇
- 아웃게임
- 분석과 모니터링
   - CPU 사용량이 임계치에 도달했을 때 알림을 받거나 지속적으로 기록되는 로그를 분석하고 리포팅 하는데 서버리스를 사용
   -  하루 1억건의 이벤트 처리와 데이터 분석 리포팅에 서버리스를 적용해 84%의 비용을 절감

</div>
<div>

- 자동화 작업
   - 동영상 업로드 시 파일의 인코딩과 검증, 태깅 이후에 공개되는 작업을 서버리스를 통해 자동화
   - 동영상의 유해성 여부를 확인하는 기능을 서버리스로 운영
- 배치 작업
   - 데이터를 실시간으로 처리하는게 아니라, 일괄적으로 모아서 처리하는 작업인 배치 작업의 경우 24시간 운영되던 서버가 필요 없으며, 특정 시간에 수행되던 기능을 서버리스로 구현하면 효율적

</div>
</div>

<BarBottom  title="Serverless right now!">
  <Item text="seongs1024/serverless-right-now">
    <carbon:logo-github />
  </Item>
  <Item text="seongspa">
    <img
      src="https://42.fr/wp-content/uploads/2021/05/42-Final-sigle-seul.svg"
      class="w-5"
    />
  </Item>
</BarBottom>

---
layout: intro
---

## 서버리스 아키텍쳐가 적합한 서비스가 있나요?

<br />
<br />

### 적합한 서비스

- 관리보다 개발에 집중하여 출시해야하는 서비스
- 함수 단위 로직으로 코드 유지보수나 기능 추가가 가능한 서비스
- 이벤트 기반 실행으로 유지비를 낮출 목적이 있는 경우
- 반복적으로 타 시스템과 연계하여 비즈니스 인사이트를 도출해야하는 서비스

<br />

### 적합하지 않은 서비스

- 장기간 지속 작업에는 부적합
- 웹소켓처럼 상시 컨넥트 되어야하는 서비스
- 콜드스타트를 허용할 수 없는 서비스
- 서비스 처리 결과에 대한 데이터 저장 필요한 경우

<BarBottom  title="Serverless right now!">
  <Item text="seongs1024/serverless-right-now">
    <carbon:logo-github />
  </Item>
  <Item text="seongspa">
    <img
      src="https://42.fr/wp-content/uploads/2021/05/42-Final-sigle-seul.svg"
      class="w-5"
    />
  </Item>
</BarBottom>

---
layout: intro
---

# Quiz📝

<br />

## 1. 서버리스 모델 명칭 두 가지(`____` 그리고 `____`)

<br />

## 2. 서버리스 장단점 한 가지씩

<BarBottom  title="Serverless right now!">
  <Item text="seongs1024/serverless-right-now">
    <carbon:logo-github />
  </Item>
  <Item text="seongspa">
    <img
      src="https://42.fr/wp-content/uploads/2021/05/42-Final-sigle-seul.svg"
      class="w-5"
    />
  </Item>
</BarBottom>

---
layout: intro
---

# Part 2. Hands-on labs

---
layout: image-right
image: ./figures/diagram.png
---

## PRODUCT:

Hello World Serverless ver.

<br />

## TECH STACKS:

|     |     |
| --- | --- |
| language | <kbd>Python</kbd> |
| event sourcing | <kbd>AWS EventBridge</kbd> |
| computing | <kbd>AWS Lambda</kbd> |
| interaction | <kbd>Slack API</kbd> |

<BarBottom  title="Serverless right now!">
  <Item text="seongs1024/serverless-right-now">
    <carbon:logo-github />
  </Item>
  <Item text="seongspa">
    <img
      src="https://42.fr/wp-content/uploads/2021/05/42-Final-sigle-seul.svg"
      class="w-5"
    />
  </Item>
</BarBottom>

---
layout: image-right
image: ./figures/inst1.png
---

## 0) Slack 앱 생성

<br />

Slack에 `serverless-right-now` 이름으로 새 워크스페이스를 개설합니다.

Slack API 페이지를 방문해 `Create an app`을 누릅니다.

`From scratch`를 누릅니다.

앱 이름을 `RightNow`로 설정하고, 새로 만든 워크스페이스를 선택합니다.

<BarBottom  title="Serverless right now!">
  <Item text="seongs1024/serverless-right-now">
    <carbon:logo-github />
  </Item>
  <Item text="seongspa">
    <img
      src="https://42.fr/wp-content/uploads/2021/05/42-Final-sigle-seul.svg"
      class="w-5"
    />
  </Item>
</BarBottom>

---
layout: image-right
image: ./figures/inst2.png
---

## 1) Webhooks URL 생성

<br />

`Incoming Webhooks` 기능페이지로 들어옵니다.

기능을 활성화 시키고, `Add New Webhook to Workspace`를 눌러서 URL을 생성합니다.

<BarBottom  title="Serverless right now!">
  <Item text="seongs1024/serverless-right-now">
    <carbon:logo-github />
  </Item>
  <Item text="seongspa">
    <img
      src="https://42.fr/wp-content/uploads/2021/05/42-Final-sigle-seul.svg"
      class="w-5"
    />
  </Item>
</BarBottom>

---
layout: image-right
image: ./figures/inst3.png 
---

## 2) Lambda 함수 생성

<br />

AWS Console에 로그인한 뒤, Lambda 페이지에 들어옵니다.

함수 생성 버튼을 누릅니다.

이름과 런타임을 설정해서 함수를 생성합니다.

<BarBottom  title="Serverless right now!">
  <Item text="seongs1024/serverless-right-now">
    <carbon:logo-github />
  </Item>
  <Item text="seongspa">
    <img
      src="https://42.fr/wp-content/uploads/2021/05/42-Final-sigle-seul.svg"
      class="w-5"
    />
  </Item>
</BarBottom>

---

## 3) Layers - 아카이브 생성

<br />

<div class="grid grid-cols-2 gap-x-4">
<div>

### Python 가상 환경을 생성합니다.
```shell
python -m venv lambda_venv
```
<br />

### 가상 환경을 활성화 시킵니다.
```shell
# [On Ubuntu]
source lambda_venv/bin/activate

# [On Windows]
.\lambda_venv\Scripts\activate
```

</div>
<div>

### ⚠️중요! `python` 이름으로 폴더를 만듭니다.
```shell
mkdir python
```

<br />

### `requests` 패키지를 다운받습니다.
```shell
pip install requests -t python
```

<br />

### 아카이빙해줍니다.
```shell
# [On Ubuntu]
zip -r requests.zip python

# [On Windows]
powershell Compress-Archive python requests.zip
```
</div>
</div>

<BarBottom  title="Serverless right now!">
  <Item text="seongs1024/serverless-right-now">
    <carbon:logo-github />
  </Item>
  <Item text="seongspa">
    <img
      src="https://42.fr/wp-content/uploads/2021/05/42-Final-sigle-seul.svg"
      class="w-5"
    />
  </Item>
</BarBottom>

---
layout: image-right
image: ./figures/inst4.png
---

## 4) Layers 생성

<br />

오른쪽 탭에 있는 Layers 페이지에 들어갑니다.

레이어 생성 버튼을 누릅니다.

이름, zip 파일, 런타임을 설정합니다.

생성하기 버튼을 클릭합니다.

<BarBottom  title="Serverless right now!">
  <Item text="seongs1024/serverless-right-now">
    <carbon:logo-github />
  </Item>
  <Item text="seongspa">
    <img
      src="https://42.fr/wp-content/uploads/2021/05/42-Final-sigle-seul.svg"
      class="w-5"
    />
  </Item>
</BarBottom>

<BarBottom  title="Serverless right now!">
  <Item text="seongs1024/serverless-right-now">
    <carbon:logo-github />
  </Item>
  <Item text="seongspa">
    <img
      src="https://42.fr/wp-content/uploads/2021/05/42-Final-sigle-seul.svg"
      class="w-5"
    />
  </Item>
</BarBottom>

---
layout: image-right
image: ./figures/inst5.png
---

## 5) Layers 추가

<br />

Lambda Functions 페이지로 돌아와 만들었던 함수에서 Layers를 선택합니다.

레이어 추가 버튼을 누릅니다.

커스텀 레이어를 고른 뒤, 만들어준 레이어와 버전을 선택합니다.

추가하기 버튼을 클릭합니다.

<BarBottom  title="Serverless right now!">
  <Item text="seongs1024/serverless-right-now">
    <carbon:logo-github />
  </Item>
  <Item text="seongspa">
    <img
      src="https://42.fr/wp-content/uploads/2021/05/42-Final-sigle-seul.svg"
      class="w-5"
    />
  </Item>
</BarBottom>

---

## 6) 함수 작성

<br />

<div class="grid grid-cols-2 gap-x-4">
<div>

에디터에 코드를 작성합니다.

<br />

⚠️중요!

코드를 작성한 뒤, `Deploy` 버튼을 눌러 저장하세요!

</div>
<div>

### ❗ environment variables configuration 필요

```python
import json
import os
import requests

def lambda_handler(event, context):
    url = os.environ['WEBHOOK_URL']
    header = {'Content-Type': 'application/json'}
    payloads = {'text': 'Hello from Lambda!'}
    res = requests.post(url, headers = header,
        data = json.dumps(payloads)
    )
    body = {
        'url': url,
        'message': payloads,
        'response': res.text,
    }
    return {
        'statusCode': res.status_code,
        'body': json.dumps(body)
    }
```

</div>
</div>

<BarBottom  title="Serverless right now!">
  <Item text="seongs1024/serverless-right-now">
    <carbon:logo-github />
  </Item>
  <Item text="seongspa">
    <img
      src="https://42.fr/wp-content/uploads/2021/05/42-Final-sigle-seul.svg"
      class="w-5"
    />
  </Item>
</BarBottom>

---
layout: image-right
image: ./figures/inst6.png
---

## 7) 환경변수 설정

<br />

Configuration 탭에서 환경변수를 눌러줍니다.

환경변수 추가 버튼을 선택합니다.

키로 `WEBHOOK_URL`, 값으로 Slack incoming webhook url을 넣어줍니다.

<BarBottom  title="Serverless right now!">
  <Item text="seongs1024/serverless-right-now">
    <carbon:logo-github />
  </Item>
  <Item text="seongspa">
    <img
      src="https://42.fr/wp-content/uploads/2021/05/42-Final-sigle-seul.svg"
      class="w-5"
    />
  </Item>
</BarBottom>

---
layout: image-right
image: ./figures/inst7.png
---

## 8) 테스트

<br />

에디터로 돌아와 테스트 버튼을 누릅니다.

새 테스트 이벤트 만들기를 선택합니다.

테스트 이름을 적고 저장합니다.

테스트 버튼을 눌러 테스트 해봅니다.

<BarBottom  title="Serverless right now!">
  <Item text="seongs1024/serverless-right-now">
    <carbon:logo-github />
  </Item>
  <Item text="seongspa">
    <img
      src="https://42.fr/wp-content/uploads/2021/05/42-Final-sigle-seul.svg"
      class="w-5"
    />
  </Item>
</BarBottom>

---
layout: image-x
image: ./figures/rightnow.png
imageOrder: 1
---

Lambda로부터 메시지가 잘 오는군요!

<BarBottom  title="Serverless right now!">
  <Item text="seongs1024/serverless-right-now">
    <carbon:logo-github />
  </Item>
  <Item text="seongspa">
    <img
      src="https://42.fr/wp-content/uploads/2021/05/42-Final-sigle-seul.svg"
      class="w-5"
    />
  </Item>
</BarBottom>

---
layout: image-right
image: ./figures/diagram2.png
---

## Slack으로 함수 요청

<br />

사용자가 슬랙에 명령어를 입력하면 HTTP 요청을 통해 Lambda 함수를 인보크해겠습니다.

⚠️ Lambda 함수의 URL을 바로 사용하는 것이 아닌 API Gateway를 통해서 HTTP 요청을 하는 것이 안전합니다.

<BarBottom  title="Serverless right now!">
  <Item text="seongs1024/serverless-right-now">
    <carbon:logo-github />
  </Item>
  <Item text="seongspa">
    <img
      src="https://42.fr/wp-content/uploads/2021/05/42-Final-sigle-seul.svg"
      class="w-5"
    />
  </Item>
</BarBottom>

---
layout: image-right
image: ./figures/inst9.png
---

## 9) Function URL 생성

<br />

Configuration 탭에서 Function URL을 선택합니다.

Auth type으로 NONE을 선택하고 저장합니다.

생성된 url을 복사해둡니다.

<BarBottom  title="Serverless right now!">
  <Item text="seongs1024/serverless-right-now">
    <carbon:logo-github />
  </Item>
  <Item text="seongspa">
    <img
      src="https://42.fr/wp-content/uploads/2021/05/42-Final-sigle-seul.svg"
      class="w-5"
    />
  </Item>
</BarBottom>

---
layout: image-right
image: ./figures/inst10.png
---

## 10) Slack App Slash Commands 등록

<br />

Slack App 설정 페이지에서 Slash Commands 기능페이지로 갑니다.

새로운 커맨드 생성 버튼을 누릅니다.

`/greetings` 커맨드를 입력하고 Requete URL에 복사해둔 function url을 붙여넣습니다.

설명란을 간단히 채웁니다.

저장하기 버튼을 클릭합니다.

Slash command가 등록된 것을 확인합니다.

슬랙 채널로 돌아와 `/greetings`를 입력하면 Lambda 함수가 실행되는 것을 확인할 수 있습니다.

<BarBottom  title="Serverless right now!">
  <Item text="seongs1024/serverless-right-now">
    <carbon:logo-github />
  </Item>
  <Item text="seongspa">
    <img
      src="https://42.fr/wp-content/uploads/2021/05/42-Final-sigle-seul.svg"
      class="w-5"
    />
  </Item>
</BarBottom>

---
layout: image-right
image: ./figures/diagram3.png
---

## 일정한 주기로 함수 인보크

<br />

EventBridge를 통해 cron 규칙을 생성하고 일정 시간마다 Lambda 함수를 실행시켜보겠습니다.

<BarBottom  title="Serverless right now!">
  <Item text="seongs1024/serverless-right-now">
    <carbon:logo-github />
  </Item>
  <Item text="seongspa">
    <img
      src="https://42.fr/wp-content/uploads/2021/05/42-Final-sigle-seul.svg"
      class="w-5"
    />
  </Item>
</BarBottom>

---
layout: image-right
image: ./figures/inst11.png
---

## 11) 트리거 설정

<br />

Lambda 함수 오버뷰에서 트리거 추가 버튼을 누릅니다.

드롭다운 목록에서 EventBridge를 선택합니다.

새 규칙 추가하기 라디오 버튼을 선택합니다.

규칙의 이름을 설정합니다.

규칙 종류로 Schedule expression을 선택합니다.

크론식을 적고 저장합니다.


<BarBottom  title="Serverless right now!">
  <Item text="seongs1024/serverless-right-now">
    <carbon:logo-github />
  </Item>
  <Item text="seongspa">
    <img
      src="https://42.fr/wp-content/uploads/2021/05/42-Final-sigle-seul.svg"
      class="w-5"
    />
  </Item>
</BarBottom>

---
layout: image-x
image: ./figures/cron.png
imageOrder: 1
---

# 😍

<BarBottom  title="Serverless right now!">
  <Item text="seongs1024/serverless-right-now">
    <carbon:logo-github />
  </Item>
  <Item text="seongspa">
    <img
      src="https://42.fr/wp-content/uploads/2021/05/42-Final-sigle-seul.svg"
      class="w-5"
    />
  </Item>
</BarBottom>

---

## ⚠️💸중요! 리소스 폐기 꼭 하세요. 비용이 지불됩니다.💸⚠️

<br />
<br />
<br />

- 🗑️ AWS EventBridge
- 🗑️ AWS Lambda

<BarBottom  title="Serverless right now!">
  <Item text="seongs1024/serverless-right-now">
    <carbon:logo-github />
  </Item>
  <Item text="seongspa">
    <img
      src="https://42.fr/wp-content/uploads/2021/05/42-Final-sigle-seul.svg"
      class="w-5"
    />
  </Item>
</BarBottom>

---
layout: intro
---

# Ask me anything

<BarBottom  title="Serverless right now!">
  <Item text="seongs1024/serverless-right-now">
    <carbon:logo-github />
  </Item>
  <Item text="seongspa">
    <img
      src="https://42.fr/wp-content/uploads/2021/05/42-Final-sigle-seul.svg"
      class="w-5"
    />
  </Item>
</BarBottom>

---

## 시간관계상 더 나누지 못한 이야기

<br />
<br />

- 실습에서 만든 슬랙 앱을 퍼블릭하게 배포하고 여러 워크스페이스에서 사용가능하게 만들려면 아키텍쳐를 어떻게 수정해야할까?
- [서버리스 아키텍쳐에서는 블루/그린 전략, 카나리아 배포를 어떻게 할 수 있을까?](https://aws.amazon.com/ko/getting-started/deep-dive-serverless/)

<BarBottom  title="Serverless right now!">
  <Item text="seongs1024/serverless-right-now">
    <carbon:logo-github />
  </Item>
  <Item text="seongspa">
    <img
      src="https://42.fr/wp-content/uploads/2021/05/42-Final-sigle-seul.svg"
      class="w-5"
    />
  </Item>
</BarBottom>

---
layout: intro
---

# 감사합니다!

<BarBottom  title="Serverless right now!">
  <Item text="seongs1024/serverless-right-now">
    <carbon:logo-github />
  </Item>
  <Item text="seongspa">
    <img
      src="https://42.fr/wp-content/uploads/2021/05/42-Final-sigle-seul.svg"
      class="w-5"
    />
  </Item>
</BarBottom>

---

## 참고

<br />

- AWS 공식 문서
- [서버리스란?](https://tech.weperson.com/wedev/backend/serverless/#serverless)
- [서버리스 사용 사례](https://inpa.tistory.com/entry/WEB-%F0%9F%8C%90-%EC%84%9C%EB%B2%84%EB%A6%AC%EC%8A%A4ServerLess-%EA%B0%9C%EB%85%90-%F0%9F%92%AF-%EC%B4%9D%EC%A0%95%EB%A6%AC-BaaS-FaaS)
- [서버리스가 적합한 경우](https://cloudmt.co.kr/?p=3774)
