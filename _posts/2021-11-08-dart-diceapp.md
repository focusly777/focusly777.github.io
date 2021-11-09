---
title: "[dart&flutter] 주사위앱만들기 (Expanded,StatefulWidget,랜덤번호생성) "
categories: 
  - dart
  - flutter
  - dart class
tags: 
  - flutter
  - dart
  - Dr. Angela Yu
  - 강의
  - 문법
  - 변수
  - expanded
toc: true
toc_sticky: true

---



## 주사위앱 만들기를 통해 배울수있는 개념

- 주사위앱

<img src="/assets/img/diceapp.gif" alt="diceapp" style="zoom:100%;" />

### Expanded

expanded로 균형잡힌 배열가능



### StatefulWidget

```dart
class DicePage extends StatefulWidget {
  @override //statefulwidget으로 설정
  _DicePageState createState() => _DicePageState();
}

class _DicePageState extends State<DicePage> {
  int leftDiceNumber = 1; // 첫시작 주사위 변수 지정
  int rightDiceNumber = 1; // 첫시작 주사위 변수 지정
```



### int 변수

```dart
  int leftDiceNumber = 1; // 첫시작 주사위 변수 지정
  int rightDiceNumber = 1; // 첫시작 주사위 변수 지정
```



### 함수모음 함수 생성

```dart
void changeDiceFace() {
    setState(() {
      leftDiceNumber = Random().nextInt(6) + 1;
      rightDiceNumber = Random().nextInt(6) + 1;
    });
  } // 함수모음함수
```



### 무작위(랜덤)번호생성

```dart
      leftDiceNumber = Random().nextInt(6) + 1;//왼쪽랜덤주사위번호생성
      rightDiceNumber = Random().nextInt(6) + 1;//오른쪽랜덤주사위번호생성
```





## 주사위앱 전체소스코드

```dart
import 'dart:math';
import 'package:flutter/material.dart';

void main() {
  return runApp(
    MaterialApp(
      debugShowCheckedModeBanner: false,
      home: Scaffold(
        backgroundColor: Colors.yellow[600],
        appBar: AppBar(
          title: Text(
            'DICE APP',
            style: TextStyle(
              color: Colors.white,
            ),
          ),
          backgroundColor: Colors.black87,
        ),
        body: DicePage(),
      ),
    ),
  );
}

class DicePage extends StatefulWidget {
  @override //statefulwidget으로 설정
  _DicePageState createState() => _DicePageState();
}

class _DicePageState extends State<DicePage> {
  int leftDiceNumber = 1; // 첫시작 주사위 변수 지정
  int rightDiceNumber = 1; // 첫시작 주사위 변수 지정

  void changeDiceFace() {
    setState(() {
      leftDiceNumber = Random().nextInt(6) + 1;//왼쪽랜덤주사위번호생성
      rightDiceNumber = Random().nextInt(6) + 1;//오른쪽랜덤주사위번호생성
    });
  } // 함수모음함수

  @override
  Widget build(BuildContext context) {
    return Center(
      child: Row(
        children: [
          Expanded(
            // Expanded로 양쪽균형잡히게 배열
            child: FlatButton(
              child: Image.asset(
                'images/dice$leftDiceNumber.png',
              ),
              onPressed: () {
                changeDiceFace(); //지정한함수
              },
            ),
          ),
          Expanded(
            // Expanded로 양쪽균형잡히게 배열
            child: FlatButton(
              child: Image.asset(
                'images/dice$rightDiceNumber.png',
              ),
              onPressed: () {
                changeDiceFace(); //지정한함수
              },
            ),
          ),
        ],
      ),
    );
  }
}

```

