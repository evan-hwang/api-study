## 7. 간결하고 체계적인 API 디자인하기

"적을수록 좋다."

"모든 물건은 맞는 자리에 있어야한다."



### 7.1 API 구조화

*논리적으로 그룹화되고 정렬된 경우 원하는 요소를 쉽게 찾아내고 그 목적도 이해하기 쉽게 해준다.*



#### 7.1.1 데이터 구조화하기

문제되는 데이터 구조

```json
{
	"overdraftProtectin": true,
	"age": 3,
	"type": 2,
	"safeToSend": 600,
	"typeName": "checking",
	"balnce": 500,
	"limit": 100
}
```



1. 위치를 통한 연관성 부여

```json
{
	"overdraftProtectin": true, // <-
  "limit": 100, 							// <-
	"age": 3,
	"type": 2,
	"safeToSend": 600,
	"typeName": "checking",
	"balnce": 500
}
```



2. 이름을 통한 연관성 부여

```json
{
	"overdraftProtectin": true, // <-
  "overdraftLimit": 100,			// <-
	"age": 3,
	"type": 2,
	"safeToSend": 600,
	"typeName": "checking",
	"balnce": 500
}
```



3. 하위 구조를 통한 연관성 부여

```json
{
  "overdraftProtection": { // <-
    "active": true,
    "limit": 100,			
  },
	"age": 3,
	"type": 2,
	"safeToSend": 600,
	"typeName": "checking",
	"balnce": 500
}
```



4. 중요한 데이터 순으로 배치

```json
{
  "typeName": "checking",
  "type": 2,
	"safeToSend": 600,
	"balnce": 500,
  "overdraftProtection": {
    "activ": true,
    "limit": 100,			
  },
	"age": 3
}
```



#### 7.1.2 피드백 구조화하기

생략



#### 7.1.3 목표 구조화하기

생략



---

### 7.2 API 사이징

*"하나의 API 라고 생각했던 것을 다른 여러 개로 나누는게 더 가치있을 수 있다."*



#### 7.2.1 데이터 세분화 선택하기

요청이나 응답의 바디는 다음의 형태를 추천한다.

- 속성의 개수를 최대한 줄여라.
- 깊이는 3단계 미만으로 유지하라.



#### 7.2.2 목표 세분화 선택하기

목표를 사용성에 맞게 세분화하자.



#### 7.2.3 API 세분화 선택하기

생략

