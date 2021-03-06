# 2장. OAuth 2.0의 기본



## 2.1 OAuth 2.0 프로토콜의 개요: 토큰 획득과 사용

**OAuth 트랜젝션의 2개의 중요한 단계**

1. 토큰의 발급
2. 토큰의 사용

**토큰:** 클라이언트에게 위임된 접근 권한을 의미하기도 함.

1. `리소스 소유자`는 `클라이언트`에게 자신을 대신해 작업을 수행하도록 요청.
2. 클라이언트는 `인가 서버`의 `리소스 소유자`에게 인가를 요청.
3. `리소스 소유자`는 `클라이언트`를 인가함
4. `클라이언트`는 `인가 서버`로 부터 토큰을 전달받음
5. `클라이언트`는 `보호된 리소스`에 접근하기 위해 토큰을 사용함.





## 2.2 OAuth 2.0 인가 그랜트<sup>(Authorization Grant)</sup>

* 리소스 소유자가 인가 서버에 직접 인증하므로 클라이언트에 사용자 인증 정보가 공유되지 않음.

* ...

  

## 2.3 OAuth의 구성원: 클라이언트, 인가 서버, 리소스 소유자 그리고 보호된 리소스

* **클라이언트**
  * 리소스 소유자를 대신해 보호된 리소스에 접근하고자 하는 소프트웨어
  * OAuth 시스템의 가장 단순한 구성요소
* **보호된 리소스** 
  * HTTP 서버를 통해접근
  * 접근을 위해 OAuth 토큰이 필요함.
* **리소스 소유자**
  * 클라이언트에게 접근권한을 위임할 권한을 가짐.
  * 소프트웨어가 아님, 대부분의 경우 소프트웨어를 사용하는 사람.
* **인가 서버**
  * HTTP 서버로서 OAuth의 핵심 구성원
  * 리소스 소유자와 클라이언트를 인증
  * 리소스 소유자가 클라이언트에게 권한을 위임할 수 있는 메카니즘 제공
  * 클라이언트에 토큰 발급



## 2.4 OAuth의 구성요소: 토큰, 범위 그리고 인가 그랜트



### 2.4.1 액세스 토큰 

* 간단히 토큰이라함.

* 인가 서버가 클라이언트에게 발급

* 클라이언트에게 부여된 권한을 나타냄

* 클라이언트는 토큰 자체를 분석할 필요가 없음

  * 그래서 클라이언트가 단순해질 수 있음.

  * 그러나 인가 서버와 보호된 리소스는 전달된 토큰 이해하고 검증함.

    



### 2.4.2 범위

* 보호된 리소스에 대한 접근 권한을 나타냄
* 공백으로 구분된 범위 문자열의 조합으로 표현됨.



### 2.4.3 리프레시 토큰 

* 클라이언트는 발급받은 토큰의 내용이 무엇인지 알지못하거나 개의치 않는 점에서 엑세스 토큰과 유사함.
  * 차이점은.. 리프레시 토큰은 보호된 리소스에 전달되지 않는다는 점.
* 클라이언트는 리소스 소유자와는 상관 없이 리프레시 토큰을 이용해 새로운 토큰을 요청함.



### 2.4.4 인가 그랜트

* OAuth의 전체 프로세스를 의미함.

  * 클라이언트가 사용자를 인가 엔드포인트로 이동시키고, 인가 코드를 전달 받고, 마지막으로 인가 코드를 토큰과 교환하는 과정 전체를 의미함.

  





## 2.5 OAuth의 구성원과 구성요소 간의 상호 작용: 백 채널, 프런트 채널 그리고 엔드 포인트



### 2.5.1 백 채널 통신

* 브라우저를 제외한 구성요소 간의 직접적인 HTTP 연결을 이용하는 것.

  * 리소스 소유자의 직접적인 개입이 없는... 그외 OAuth 구성요소간의 HTTP API 통신을 말하는 것 같다..

  

### 2.5.2 프런트 채널 통신

* 두 구성요소가 직접 HTTP 요청을 보내고 응답을 받지 않는 경우.
* 중간의 웹 브라우저를 통해 두 시스템이 간접적으로 HTTP 통신을 하는 방법
  * 웹 브라우저가 방문해야하는 URL을 파라미터로 전달함으로서 이루어짐. (URL 리다이렉트)



## 2.6 요약

* ...





## 의견 

1장에 상태보다는 좀더 이해가 되는 것 같다.

다음 장 부터는 코드로도 설명을 하시는 것 같은데... 더 나아질 것 같다. 😄





## 단어

* [메커니즘](https://ko.dict.naver.com/#/entry/koko/c1d0c49461b549c8934ac82fe52c2450)
  * 사물의 작용 원리나 구조



## 정오표

* ...
