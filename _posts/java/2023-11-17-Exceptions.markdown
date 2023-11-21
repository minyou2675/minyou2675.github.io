---
title:  "Exceptions"
excerpt: "Java의 Exceptions에 대해서"

categories:
  - Java
tags:
  - [Spring, java]

toc: true
toc_sticky: true
 
date: 2023-11-17
last_modified_at: 2023-11-17
---

아래의 글은 Oracle의 Java 공식문서를 기반으로 정리한 글입니다.

## Exception이란?
Exception은
메소드내 에러가 발생할 시 **Exception Object**를 생성하게 된다.
위 객체는 에러의 type과 에러 발생때 프로그램의 상태에 대한 정보를 담고있다. 

Exception이 발생할 시 **Runtime system**은 에러를 처리하기 위해 메소드를 호출하게 되고 이 메소드들은 에러가 발생한 메소드에 접근한다. 이렇게 형성된 메소드 리스트들을 
**Call stack**이라고 한다.

![image](https://github.com/minyou2675/couple_diary_project/assets/62383521/d81a34ba-f3a8-49ea-9fc8-3dd99c8dc894)
_callstack_

**런타임 시스템**은 call stack을 수색하면서 exception을 처리할 수 있는 코드를 가지고 있는 메소드를 찾는다. excepiton을 처리하는 코드를 **Exception handler**라고 한다. 수색은 메소드에서 에러 발생 뒤 호출되는 메소드 순서와 반대로 진행된다. 이 과정에서 발생한 오류로 인한 exeption object의 type과 맞는 type을 가진 handler를 적합한 exception hanlder로 찾게 된다. 

![image](https://github.com/minyou2675/couple_diary_project/assets/62383521/0be7d49f-465e-4ffd-bbe3-737eb3064a6a)
_Exception handler를 call stack에서 찾는 과정_

exception hanlder를 선택하는 것은 예외를 적절하게 처리하기 위해서다 만약 적합한 exception handler를 찾지 못하게 된다면 runtime system(결과적으로는 프로그램)은 종료된다.

## 한 걸음 더 
* Exception object가 발생할 때 호출되는 메소드는 어디에서 오는 메소드일까?
* Exception handler는 Exception object를 어떻게 처리할까?

## The Catch or Specify 요구사항

유효한 자바 프로그래밍 언어는 반드시 Catch or Specify 요구사항을 준수해야 한다. 

**try문**은 exception 발생을 포착한다. try문은 반드시 **Exception**에 대한 핸들러를 제공해야 한다. 메소드는 **throws**문을 제공하여 exception을 list화하고 발생할 수 있는 exception을 명시한다. Catch,Specify 요구를 준수하지 못하는 코드는 컴파일되지 않는다.

## 세 가지 종류의 Exceptions
첫번째 Exception은 **Checked Exception**이다. 잘 작성된 어플리케이션은 예외조건들을 예상하고 회복할 줄 알아야한다. 사용자가 특정 file을 열려고 할 때 **Constructor**는 **java.io.FileReader**에 파일 이름을 전송하게 된다. 만약 잘못된 파일 이름으로 파일을 열려고 할 경우에는 constructor는 **java.io.FileNotFoundException**을 throw 하게된다. 잘 작성된 프로그램은 예외사항을 잘 catch하고 사용자의 실수를 잘 알아차려야 한다.

Checked exceptions은 Catch or Specify 요구사항의 주요 대상이다. **Error**와 **RuntimeException**를 포함한 서브클래스를 제외한 모든 exceptions은 checked exception이다. 

두번째는 **Error**이다. 이러한 예외조건은 어플리케이션 외적인 부분이다. 그리고 어플리케이션은 예상하거나 회복하지 못한다. 예를 들면, 하드웨어나 시스템 오류로 인해 파일을 열지 못할 경우에는 java.io.IOError가 발생하게 된다. 어플리케이션은 이러한 예외사항을 catch하는 걸 선택할 수 있지만 **stack trace**를 출력하고 종료되는 것이 타당할 수도 있다.

Error는 Catch or Specify 요구사항의 대상이 되진 않는다. Error는 Error와 그의 서브 클래스에 의해 인지되는 Exceptions이다.

세번째 exception은 **runtime exception**이다. 이것은 어플리케이션 내부 예외조건에 해당한다, 그리고 쉽게 예측하거나 회복하지 못한다. 주로 로직 에러나 부적절한 API 사용으로 인한 프로그래밍 버그이다. 예를 들면, FileReader 생상자가 null 값을 전달받으면, 생성자는 **NullPointerException**같은 오류를 발생시킬 것이다. 어플리케이션이 이러한 exception은 catch 할수도 있겠지만, 종료시키는 것이 더 납득될 것이다.

Runtime exception은 Catch or Specify 요구사항의 대상이 아니다. Runtime exception은 **RuntimeException**과 그것의 하위 클래스이다.



Errors와 runtime exceptions은 종합적으로 unchecked exceptions으로 구분된다.



## 출처
https://docs.oracle.com/javase/tutorial/essential/exceptions/definition.html