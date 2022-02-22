---
title: "Classes and Structs"
categories:
    - Swift
tags:
    - class
    - struct
    
---
## Class와 Struct

프로그램 코드를 구조화 하기 위해 쓰임. 

#### Class와 Struct의 공통점
- 값을 저장하기 위해 properties를 정의 할 수 있다.
- 기능 제공을 위한 method를 정의 할 수 있다.
- .을 이용하여 내부의 property와 method에 접근 할 수 있다.
- 초기 상태를 set up 할 수 있는  initializers를 정의한다.

#### Class만의 특징은 다음과 같다. 
- 상속을 통해 클래스의 속성을 다른 클래스에게 물려 줄 수 있다.
- 타입캐스팅을 통해 런타임시 클래스의 인스턴스 타입을 확인 할 수 있다.
- 소멸자(deinit)를 통해 할당된 자원을 free up 할 수 있다.
- ARC로 메모리를 관리


#### Class와 Struct의 차이점
- Struct는 값타입이고 Class는 참조타입이다.


참조타입과 값타입이 무엇인지 쉽게 이해 할 수 있는 쉬운 예제를 보자.

```swift
  class BankAccountClass {
    var accountBalance: Float = 0
    var accountNumber: Int = 0
}

  struct BankAccountStruct {
    var accountBalance: Float = 0
    var accountNumber: Int = 0
}

var class1 = BankAccountClass()
var class2 = class1
var class3 = class2

class3.accountBalance = 10000.0     // class3의 accountBalance변경
class1.accountBalance   // 10000
class2.accountBalance   // 10000
class3.accountBalance   // 10000

var struct1 = BankAccountStruct()
var struct2 = struct1
var struct3 = struct2

struct3.accountNumber = 1103214567      // struct3의 accountNumber변경
struct1.accountNumber   // 0
struct2.accountNumber   // 0
struct3.accountNumber   // 1103214567

```


