---
title: "[dart] function 사용하기/만들기"
show_date: true
categories:
  - dart
  - flutter
tags:
  - dart 문법
  - dart
  - widget
  - function
toc: true
toc_sticky: true
---



dart를 이용해서 'hello uju'를 출력해보자



#### function 사용 (기존에 있는 것들)



이때 'print'라는 기능을 사용해야하는데 이러한 print같은 것들을 function이라고 부른다.



```dart
main(){
  pint('Hello, UJU');
} // function을 사용 하는것
```



#### function 만들기 



 그럼 function을 단순히 사용하지말고, 내가 function을 만들어서 출력해보자



####  function만들때 function 구조예시



![function_dart](/assets/img/function_dart.png)

```dart
main(){
  myPrint('Hello, UJU');
} 
myPrint(String text){
  print(text);
}
```



#### 한줄 function 간단하게 표시하는법 (=>)

function중에서 여러줄로 구성된 function이 아닌 한줄짜리 function이라면, 간단하게 표현할수있다.

```dart
int timesTwo(int x) {
  return x * 2;
}
```

이렇게 한줄짜리 function이 있다면, 중괄호를 없애고 return 대신 =>를 쓰면 된다.

 ```dart
int timesTwo(int x)   => x * 2;
 ```

끝!

 ```dart
//정리

int timesTwo(int x) {
  return x * 2;
} 
//중괄호를 없애고 return을 =>로 바꿔준다.

int timesTwo(int x)   => x * 2;
//위 함수와 동일한 함수가 되지만 간단하게 표현가능하다.

 ```





아래는 연습노트입니다. (무시해주세요)

똑같이 따라쓰기 무한반복중..

<hr>

```dart
main(){
  myPrint('Hello UJU');
}

myPrint(String text){
  print(text);
}
//1

main(){
  myPrint('Hello UJU');
}

myPrint(String text){
  print(text);
}

//2
main(){
  myPrint('Hello UJU 3번반복중입니다.');
}

myPrint(Spring text){
  print(text)
}
//3

mian()
  myPrint ('UJU')
```

