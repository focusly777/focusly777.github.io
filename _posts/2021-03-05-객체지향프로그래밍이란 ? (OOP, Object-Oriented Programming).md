---
title : "객체지향프로그래밍이란 ? (OOP, Object-Oriented Programming)"
permalink: /oop-dart/
categories: 
  - 객체지향프로그래밍
tags: 
  - 객체지향프로그래밍
  - OOP
  - 객체지향
  - class
  - dart
toc: true
toc_sticky: true
---

<iframe width="560" height="315" src="https://www.youtube.com/embed/vrhIxBWSJ04?start=52" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe><br><br>

## CLASS 

### CLASS에 대하여

프로그래밍에 익숙하신 분들에게 Class라는 단어는 매우 익숙한 단어일 것입니다. 그 이유는 프로그래밍에 있어서 class라는 개념이 매우매우 중요하고 자주 사용되기 때문입니다. dart 역시 공식문서에서 *‘Dart is an object-oriented language with classes and mixin-based inheritance’*라고 소개하고 있을 만큼 class는 매우 중요한 요소입니다. 지금부터 하나하나씩 살펴보겠습니다.



1. <u>다트 = 모든 것이 객체 (완전 객체 지향 언어)</u>
   1. 모든 객체 = 인스턴스of 클래스
   2. 모든 클래스는 = 자식 of Object 클래스 
      ~~(붕어빵, 붕어빵틀, 여러가지 맛의 붕어빵들을 생각하자!)~~
   3. <u>클래스는 멤버</u>를 갖는데, **<u>멤버 함수(메서드)</u>와 <u>멤버 변수(인스턴스 변수)</u>로 구성**됨.
2. 클래스를 사용하려면 객체를 생성해야 하는데,
   1. 객체를 생성한다는 것은 클래스가 메모리에 올라간다는 의미이고,
   2. 이것을 인스턴스화라고 부름.
   3. 이렇게 메모리에 클래스가 할당되어 인스턴스가 된 것을 객체라고 함!

`Function` : 클래스 외부에서 하나의 기능을 하는 함수.
`Method` : 클래스 내부에 있는 멤버 함수.
`멤버 변수`는 객체가 생성되면 `인스턴스 변수`라 함.





### CLASS의 기본 형태

```dart

main() {
	var student = new Person();
    	var teacher = Person();

}

/* class 클래스명 {
멤버 변수
멤버 함수
} */

class Person {
	String name;
    int age;
    getName() {
    	return name;
    }
}
```



객체 생성시 `new` 키워드는 생략해도 무관함.

```dart
main() {
  Person student = Person(); // var student = new Person(); 도 되지만 타입 지정 습관화!
  Person teacher = Person();

  student.name = 'CHA';
  teacher.name = 'PARK';

  print('학생 이름 = ${student.getName()}');
  print('선생님 이름 = ${teacher.getName()}');
}

/* class 클래스명 {
멤버 변수
멤버 함수
} */

class Person {
  String name;
  int age;

  getName() {
    return name;
  }
}
// 학생 이름 = CHA
// 선생님 이름 = PARK

```







### 객체지향 프로그래밍(Object-Oriented Programming)



1. **<u>변수와 함수를 하나의 주머니에 담아두는 곳이다.</u>**
2. ***class 안의 함수**를 **method** 라고 한다.*
   - 예를 들어
     - **Person** 이라는 주머니에는 **사람에 연관된 변수와 함수들**이 있다.
     - **Person** **클래스라고 정의**를 하고
     - **클래스 안에는 그 사람의 이름과 나이**가 있고
       - 그런 **데이터 타입들은 변수**로 정의를 한다.
       - 그리고 **잔다거나 일하는 행동들은 함수로 정의**를 한다.
3. *코딩을 하다보면 **<u>코드가 복잡해지고 길어지는데</u>***
4. *이럴 때 우리는 **<u>어떤 변수와 함수를 사용할지 힘들어</u>**진다.*
5. <mark><u>그럴 때, 클래스를 만들어 주면</u></mark>
6. <mark>아~ 저런 함수 이런 변수는 저 클래스에 있었지!</mark>
7. <mark>라고 머릿속에 이미지화</mark>해서 ***코딩을 좀 더 쉽게 할 수 있다.****
8. **<u>이런 코딩 방법을 <mark>객체지향 프로그래밍</mark>이라고 한다.</u>**







출처:[진주블로그](https://chajinjoo.netlify.app/posts/dart/dart17/#%ED%81%B4%EB%9E%98%EC%8A%A4%EC%9D%98-%EA%B8%B0%EB%B3%B8-%ED%98%95%ED%83%9C)
