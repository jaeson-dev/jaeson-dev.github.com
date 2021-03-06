---
title: "optional 과 unwrapping"
categories:
    - Swift
tags:
    - optional
    - unwrapping
    - if let, if var, guard let, guard var
---

Swift 언어는 타입에 굉장히 업격하다. Swift내의 여러 개의 타입중 nil 이라는 타입이 존재한다. 
nil 이라는 타입은 값이 있을 수도 있고 없을 수도 있는 타입이다. 

nil 타입으로 선언된 변수안에 담긴 값을 Int 나 String 타입등 다른 타입으로 꺼내어 쓰고 싶을 때 오류가 발생한다. 이를 해결 하기 위해서는 nil로 감싸진 타입을 벗겨내야 하는데 이를 unwrapping 이라고 한다. 

unwrapping 하는 방법은 크게 두 가지로 나뉜다. 

첫 번째는 '!' 키워드를 사용해 강제로 벗겨내는 것이다. '!' 키워드를 nil 타입의 변수 앞에 붙여 쓰면 unwrapping이 되어 해당 변수 안의 값을 꺼낼 수가 있는데 이런 경우에는 한 가지 전제 조건이 붙는다. 바로 해당 타입이 비어있지 않을 거라는 조건이다. 타입에 엄격한 swift 언어 특성상 이와 같은 방식으로 unwrapping 하는 것은 위험할 수 있다.

두 번째는 if let & if var 또는 guard let & guard var 를 사용하여 unwrapping하는 것인데 이를 Optional Binding 이라고 표현하기도 한다. 

if let 과 guard let 의 차이는 무엇일까?

if let에서는 변수가 선언된 스코프 내부에서만 사용할 수 있고 else 블록이나 기타 해당 블록 밖에서는 사용 할 수 없다.  

guard let에서 선언된 변수는 else 블록 안에서는 사용할 수 없다. 그러나 guard let 이 정의된 함수블록등 안에서는 전역변수처럼 사용이 가능하다. 
