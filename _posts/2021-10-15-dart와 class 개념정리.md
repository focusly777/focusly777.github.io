---
title: "[dart] dart와 class개념정리"
permalink: /dart-class/
categories: 
  - 객체지향프로그래밍
  - dart
  - flutter
tags: 
  - flutter
  - 클래스
  - 객체지향
  - class
  - dart
toc: true
toc_sticky: true
---

### CLASS란

프로그래밍에 익숙하신 분들에게 Class라는 단어는 매우 익숙한 단어일 것입니다. 그 이유는 프로그래밍에 있어서 class라는 개념이 매우매우 중요하고 자주 사용되기 때문입니다. dart 역시 공식문서에서 *‘Dart is an object-oriented language with classes and mixin-based inheritance’*라고 소개하고 있을 만큼 class는 매우 중요한 요소입니다. 지금부터 하나하나씩 살펴보겠습니다.



우선 dart에서 Class를 사용하는 기본 문법에 대하여 살펴보겠습니다.



## 1-1. Class 기본 문법



```dart
class Person {
  String name;
  int age;
  String gender;
}
```



<u>dart에서 class를 생성하기 위해서는 먼저 변수명 앞에</u> `class`로 <u>선언</u>해준 후 위와 같이 코드를 작성하면 됩니다. <u>그러면 Person Class는 name, age, gender와 같은 속성을 가지는 class가 됩니다.</u>



## 1-2. Class와 인스턴스의 관계

이제 Class를 생성했으니 이를 사용해야할 때입니다. Class는 main 함수 내에서 다음과 같이 사용됩니다.



```dart
void main() {
  Person p1 = Person();
  Person p2 = Person();
}
```



1. 먼저 class를 생성할 때와 같이 Person class를 변수명인 p1, p2 앞에 선언해줍니다.
2. 그리고 이렇게 생성된 p1, p2에 `Person()`이라는 생성자를 대입해주면 됩니다.
3.  이처럼 하나의 class 사용으로 p1, p2와 같은 여러개의 class 변수를 생성하였습니다.
4.  그리고 이런 class 변수를 **instance**라고 합니다.



## 1-3. Class와 생성자의 관계

프로그래밍에 익숙하지 않다면, 생성자라는 개념이 낯설 수 있습니다.

 위에서 Person Class를 만들 때 저희는 Class 내에 속성 이외에 아무것도 넣지 않았습니다. 

그런데 이런 경우 dart는 Class내에 Class명과 동일한 기본 생성자를 우리 모르게 생성해둡니다.

 따라서 저희가 p1 인스턴스를 만들 때 `Person p1 = Person();`과 같이 `Person();`생성자를 선언할 수 있는 것입니다.

 그렇다면 직접 생성자를 Class내에 생성해봅시다.



```dart
class Person {
  // 멤버 변수
  String name;
  int age;
  String gender;

  // 생성자 생성
  Person(String name, {int age, String gender}){
    this.name = name
    this.age = age
    this.gender = gender
  }
}

void main(){
    Person p1 = Person('갑', age : 20, gender : 'male');
    Person p2 = Person('을', age : 25, gender : 'female');
}
```

위의 코드에서 보시다시피 <u>class내 생성자를 만드는 방법은 함수를 생성하는 방법과 같습니다.</u> 함수와 동일하게 생성자에서도 `argument`를 받을 수 있고, `argument` 에 ‘{}’를 이용하여 옵션 값을 줄 수 있습니다. 그렇다면 Class 안에는 오직 하나의 생성자만 생성할 수 있을까요?

아닙니다 Class 내에서도 여러개의 생성자를 생성할 수 있습니다. Class내에 여러개의 생성자를 만들때에는 dot(.)을 이용해 생성자마다 각각 다른 이름을 부여해주어야 합니다.

```dart
class Person {
  String name;
  int age;
  String gender;

  // Person.one 이름의 생성자 생성
  Person.one(this.name, this.age, this.gender);
  
  // Person.two 이름의 생성자 생성
  Person.two(String name, int age, String gender){
    this.name = name;
    this.age = age;
    this.gender = gender;
  }
}

void main() {
  Person p1 = Person.one('갑', 20, 'male');
  Person p2 = Person.two('을', 25, 'female');

  print(p1.name); //갑
  print(p2.name); //을
}

```





출처:[maison de learning](https://minkithub.github.io/2020/05/12/dart1/)
