---
title: "[dart]한줄 Function 표현 팁 (=>)"
show_date: true
share: false
permalink: /onelinefunction-dart/
categories:
  - dart
tags:
  - dart
  - function
toc: true
toc_sticky: true
---

## DART에서의 Function

### 한줄 Function 표현 팁 (=>)

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

int timesTwo(int x) {
  return x * 2;
} 
//중괄호를 없애고 return을 =>로 바꿔준다.

int timesTwo(int x)   => x * 2;
//위 함수와 동일한 함수가 되지만 간단하게 표현가능하다.

 ```
