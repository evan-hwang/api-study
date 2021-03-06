## 3. 프로그래밍 인터페이스 디자인하기

이 장의 내용

- API 목표를 프로그래밍 인터페이스로 변경하기
- REST 리소스와 액션을 식별하고 매핑하기
- 컨셉으로 API 데이터 디자인하기
- REST API와 REST 아키텍처 스타일의 차이점
- API 디자인에서 REST 아키텍처 스타일이 중요한 이유

> ⚠️ 주의
>
> 이제 다룰 API 스타일은 만능이 아니다. API 스타일과 사용자의 편의성 두 가지의 절충안을 찾아야 할 때가 올 것이다.

---

### 3.1 REST API 소개

이전에 REST 하고  표현한 목표인 `GET /products/{productI}` 를 이해하는 시간이 될 것이다.



#### 3.1.1 REST API 호출 분석

`GET /products/{productI}` 리퀘스트는 HTTP 메서드와 경로로 조합된다.

HTTP 메서드

- 리소스를 가지고 무슨 행위를 하고 싶은지 표시해주는 역할

경로

- 리소스를 식별할 수 있는 주소



리스폰스는 HTTP 상태코드, 리스폰스 바디로 구성되어있다.

HTTP 상태코드

- 접수된 리퀘스트의 처리가 어떻게 되어가는지 의미
- ex) `200 OK` 

리스폰스 바디

- 리퀘스트의 경로로 식별된 리소스의 콘텐츠를 포함

  ```json
  {
  	"reference": "P123",
    "name": "Design of Web APIs",
    "price": 44.99
  }
  ```



> ⚠️ 주의
>
> HTTP 프로토콜은 단순히 JSON 데이터를 가져오려는 목적으로만 만들어진게 아니다.



#### 3.1.2 HTTP의 기초사항

위에서 다뤘듯이 요청과 응답은 HTTP 프로토콜의 구조를 따른다.



#### 3.1.3 REST API의 기초원리







---

### 3.2 API 목표를 REST API로 변형하는 과정

#### 3.2.1 API 목표 캔버스로 리소스와 리소스 사이 관계 식별

#### 3.2.2 API 목표 캔버스를 이용해 액션과 액션의 파라미터 그리고 반환값 식별

#### 3.2.3 경로를 포함한 리소스 표현

#### 3.2.4 HTTP로 액션 표현

#### 3.2.5 REST API와 HTTP 치트시트

---

### 3.3 API 데이터 디자인하기

#### 3.3.1 컨셉(Concept) 디자인

#### 3.3.2 컨셉에서 리스폰스 디자인

#### 3.3.3 컨셉과 리스폰스에서 파라미터 디자인

#### 3.3.4 데이터 소스에서 파라미터 확인

#### 3.3.5 그 외의 파라미터들 디자인

---

### 3.4 디자인적 난관에 봉착했을 때 균형 유지하는 법

#### 3.4.1 REST 절충안 예시

#### 3.4.2 사용자 편의성과 규칙 준수 균형잡기

---

### 3.5 API를 디자인할 때 REST가 중요한 이유

#### 3.5.1 REST 아키텍처 스타일 소개

#### 3.5.2 API 디자인에서의 REST 제약사항이 미치는 영향

---

### 요약