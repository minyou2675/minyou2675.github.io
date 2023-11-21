---
title:  "타입스크립트 개요"
excerpt: "타입스크립트 개념 정리"

categories:
  - Typescript
tags:
  - typescript

toc: true
toc_sticky: true
 
date: 2023-11-21
last_modified_at: 2023-11-21
---

지속 업데이트 예정

# 1. TypeScript 구성요소

### 1.자바스크립트와 타입스크립트 차이**
타입 정의
인터페이스와 클래스
null/undefined-safe
Generic(범용 클래스, 메서드 타입 적용)
편집기의 입력 자동 완성
ECMA에 정의되어 있는 자바스크립트의 최신 사양

빌드를 통해 타입스크립트 코드 -> 자바스크립트 코드로 변환

### 2.타입스크립트 CLI 설치
```
npm install -g typescript
``` 
### 3.타입스크립트 컴파일(with 엄격한 체크)
```tsc –strictNullChecks sayHello.ts```

**테스트용 REPL 도구 : TS Playground**

### 4. 타입 정의
타입 어노테이션(Type annotation)
변수나 인수명 뒤에 : 타입

### 5. 변수
var, let, const를 주로 사용
var는 전역
let은 지역
const는 값 재할당 시 오류발생
let,const를 가장 자주 사용

### 6.원시타입
* number(64비트 부동 소수점)
* string
* boolean

### 7. 배열
* number 배열 시 number[]
* string 배열 시 string[] 명시

### 8. 객체
객체는 키와 값을 이용하여 객체 타입 정의 가능
```
let object : {키명_1: 타입_1; 키명_2: 타입_2;}

```
모든 속성은 ?을 사용해 옵셔널(Optional) 속성 지정 가능
```
function printName(obj: {firstName: string; lastName?: string}) {
 // …
}
printName({ firstName: ‘Hana’ })
printName({ firstName: ‘Hana’, lastName: ‘Kim’})

```
둘 다 정상 작동

### 9.any
모든 타입을 허용 -> any 사용 시 타입 체크 기능 작동X -> any 타입 사용하지 않는 것이 바람직
```
let user: any = { firstName: ‘Hana’ }

10.함수
함수에선 인수와 반환값의 타입 지정 가능

function(인수_1: 타입_1, 인수_2: 타입_2 ….): 반환값{
//…
}

```
# 2.TypeScript 기능

## 1. 타입 추론
자동적으로 타입이 결정되는 기능(타입 어노테이션 생략하면 적용)

## 2. 타입 어서션
구체적인 타입을 알 수 없을 경우에는 타입 추론이 제대로 적용하지 않음.
이럴 경우 명시적으로 타입을 지정

변수 = 값 as 타입 

```
const myCanvas = document.getElementBy(‘main_canvas’) as HTMLCanvasElement 
```

하지만 위 같은 방식은 복잡한 어서션을 수행할 때는 잘 표현하기 어려움. 이런 경우에는 2단계 어서션으로 구현 가능

```
const result = (response as any) as User
```

단 타입 어서션은 실행 시 에러가 발생할 수 있음

3.타입 앨리어스
타입을 재사용할 경우 사용

type 타입명 = 값

```
type Point = {
	x: number,
	y: number
} 
```

3.1 인덱스 타입(키 이름 명시하지 않고 타입 앨리어스 지정가능)

{[] : 타입명 }

```
type Label = {
[key : string] : string
}
```

4.인터페이스
인터페이스를 implements 시 모든 변수와 함수의 구현을 강제함(옵셔널 속성 변수는 제외)
인터페이스는 나중에 확장 가능
인터페이스는 extends를 사용해 인터페이스를 다중상속 후 인터페이스 정의 가능
```
interface Point{
	x: number;
	y: number;
}
//추가
interface Point{
	z?: number;
}

//구현

class MyPoint implements Point{
	x: number;
	y: number;
}

// 다중 상속 후 새로운 인터페이스 정의

interface Colorful{
	color:string;
}

interface Circle{
	radius: number;
}

interface ColorfulCircle extends Colorful, Circle {}

const  cc: ColorfulCircle = {
	color: ‘빨강’,
	radius: 19
}

```
5. 클래스
클래스는 extends를 사용해 다른 클래스를 상속 가능
super 함수를 통해 상속원의 생성자를 호출할 수 있음
```
interface IUser {
	name: string;
	age: number;
	sayHello: () => string //인수없이 문자열을 반환
}

class User implements IUser{
	name: string;
	age: number;
	constructor() {
	this.name = ‘’
	this.age = 0
}

	sayHello() {
	return `안녕하세요 저는 ${this.name}이며, ${this.age}살입니다.`
}

}

```
### 6. 접근 수정자
* public: 접근 가능
* private: 접근 불가(컴파일 시 오류)
* protected: 상속후 클래스의 하위 객체만 접근 가능

# 3.실제 개발 시 도움이 되는 타입

### 1.Enum 타입
열거형, 이름이 붙은 상수 셋을 정의할 수 있음.
비슷한 기능으로는 Union, Union 타입을 선호하는 개발자도 있음
```
enum Direction {
	Up = ‘UP’,
	Down = ‘DOWN’,
	Left = ‘LEFT’,
	Right = ‘RIGHT’
	
}

const value = ‘DOWN’
// 문자열에서 Enum 타입으로 변환한다
const enumValue = value as Direction

if (enumValue == Direction.Down) {
	console.log(‘Down is selected’)
}

```
### 2. 제네릭 타입
제네릭은 클래스와 함수에 대해, 그 안에서 사용하는 타입을 추상화하여 외부에 의해 타입을 지정할 수 있는 기능

```
class Queue<T> {
	private array: T[] = []
	//T 타입의 값을 배열에 추가 
	push(item: T){
	this.array.push (item)
}
}

```
### 3. Union, Intersection 타입
타입을 조합해서 사용할 수 있으며,Union은 합집합, Intersection은 교집합의 타입
```

function printId(id: number | string){
	console.log(id)
}

// number 정상 작동
printID(11)

//string도 정상 작동
printId(‘22’)

```
### 4. 리터럴 타입
|로 구분하는 리터럴 타입을 사용하면 정해진 문자열이나 수치만 대입할 수 있는 타입으로 제어 가능
### 5.never 타입
never타입은 절대로 값이 반환되지 않는 타입을 말함

```
function error(message: string): never {
	throw new Error(message)
}

function foo(x: string | number | number []): boolean {
	if (typeof x === ‘string’) {

	return true

} else if (typeof x === ‘number’) {
	return false
}

return error(‘Never happens’)
}

```
# 4.타입스크립트 테크닉
### 1.옵셔널 체이닝
중첩된 객체의 속성이 존재하는가에 관한 조건 분기를 간단하게 기술 가능
컴파일 후 생성된 자바스크립트에 null 체크 코드를 추가하여 실행 시 에러 발생 x

만약 인터페이스에 game 속성이 있다고 할 때 객체의 game 속성에 대한 null 또는 undefined 조건을 어떻게 체크할 수 있을까?


```
interface User{
	name: string
	game?:{
		gta4: boolean
		totalwar: boolean
}
}

let user: User = {name:’Min’, game: { gta4: true, totalwar: true} } 

//game이 존재할 경우 true 출력
console.log(user.game?.gta4)

user = { name: ‘Min’ }

//game이 존재하지 않는 경우에도 에러 발생 x
console.log(user.game?.gta4) 


```

이런 방식을 통해 예외처리 발생문제나 null & undefined 분기 설정 없이 쉽게 조건 분기를 간단하게 작성이 가능하다.

### 2.논-널 어서션 연산자

컴파일 옵션 -strictNullChecks 옵션으로 컴파일시, 타입스크립트는 null일 가능성이 있는 객체에 대한 접근을 에러로 취급. 논-널 어서션 연산자는 컴파일 에러를 억제
실행 시 에러 발생 여지 있음

```
function processUser(user?: User) {
	let s = user!.name
}

```

### 3. 타입 가드
실행 시 에러를 발생시키기 쉬운 as같은 타입 어서션보다 안전하게 코드 작성 가능
if 조건문 이후 변수의 타입을 필터링(아직 좀 모호한 듯…)

### 4.keyof 연산자
### 5.인덱스 타입
### 6.readonly
### 7.unknown
### 8.비동기 Async/Await
### 9.타입 정의 파일

# 5.타입스크립트 개발 환경
### 1.tsconfig.json
### 2.Prettier
### 3.ESLint

### 6.컴파일 옵션
1.no lmplicitAny

2.target

+타입 스크립트 컴파일러
* 스캐너: 타입스크립트 소스 코드 기반 토크나이제이션
* 파서: 토큰을 받아 추상구문트리(AST) 변환
* 바인더: AST 기반 타입 체크의 기본이 되는 심벌 작성
* 체커: 타입 체크를 실행(컴파일러에서 가장 큰 부분)
* 이미터: AST와 체커의 결과를 바탕으로 타입스크립트에서 자바스크립트로 변환 후 출력




