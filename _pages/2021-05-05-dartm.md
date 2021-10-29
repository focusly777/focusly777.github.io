---
title: "dart문법 기초(쓰는중)"
categories:
  - dart
tags:
  - dart 문법
toc: true
toc_sticky: true
---

# DART에서의 변수
## Dart에서의 변수의타입
아래 변수가 있다.<sup>변수를 선언해줄때 :  변수 이름 = 변수에담을것  으로 표현을 한다. </sup> 
변수에도 타입이 있다. 타입을 지정해두지 않으면 향후 코드의 가독성이 떨어지기때문에 변수마다 변수타입을 함께 선언해주는것이 좋다. 

```dart
var name = 'Voyager I';
var year = 1977;
var antennaDiameter = 3.7;
var flybyObjects = ['Jupiter', 'Saturn', 'Uranus', 'Neptune'];
var image = {
'tags': ['saturn'],
'url': '//path/to/saturn.jpg'
}; 
//타입이 지정되지 않은 변수


String name = 'Voyager I'; // 문자
int year = 1977; // 정수
double antennaDiameter = 3.7; // 소수
List<String> flybyObjects = ['Jupiter', 'Saturn', 'Uranus', 'Neptune']; // 문자열
Map image = {
'tags': ['saturn'],
'url': '//path/to/saturn.jpg'
};
// 타입이 지정된 변수
``` 
 