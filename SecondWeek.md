# [iOS 🧟 ZOMBIE] iOS 인터뷰 - 2주차

스스로 설명할 수 있을 만큼의 인터뷰 능력을 기르는데 중점을 뒀습니다.

앨런29기 진도에 맞춰, 각 주차별로 준비한 인터뷰 문제를 풀어보고, 질문합니다.

<br>

<details>
<summary>두 개의 정수를 입력으로 받아 그 합을 반환하는 함수를 작성하십시오.</summary>

```swift
func sumTwoNumbers(_ num1: Int, _ num2: Int) -> Int {
    return num1 + num2
}
```
</details>


<details>
<summary>데이터는 RAM에 어떻게 저장됩니까?</summary>

```swift
/* 
프로그램이 실행되면 해당 프로그램이 RAM 에 로드되며 프로그램은 코드와 데이터로 구성되어 있음. -> 프로그램이 실행되는 동안 필요한 데이터는 RAM 에서 할당된다. 이 데이터는 주로 변수, 배열, 구조체 등의 형태로 표현됨. -> 주소 매핑: 각 변수나 데이터 구조는  RAM 에서 고유한 주소를 가지게 된다. 이 주소를 통해 프로그램은 해당 데이터를 읽거나 쓸 수 있음. -> CPU 는 RAM 에서 데이터를 읽어와 연산을 수행하고, 프로그램이 종료되거나 데이터가 더이상 필요하지 않을 때까지 RAM 에 저장된 데이터는 프로그램에 의해 계속해서 사용된다. 전원종료시 데이터는 소실된다. RAM 은 휘발성 메모리임으로 전원이 종료되면 저장된 데이터가 소멸된다. 컴퓨터 재부팅 및 종료될 때 발생한다.
*/
```
</details>


<details>
<summary>주어진 숫자의 제곱을 반환하는 함수를 작성하십시오.</summary>

```swift
func calculateSquare(_ number: Double) -> Double {
    return number * numer
}
```
</details>


<details>
<summary>Swift에서 지역 범위와 전역 범위의 차이점을 설명하십시오.</summary>

```swift
//답변
```
</details>


<details>
<summary>이름은 같지만 매개변수 유형이 다른 두 개의 함수를 만들어 함수 오버로딩을 구현하십시오.</summary>

```swift
//답변
```
</details>


<details>
<summary>inout 매개변수를 사용하여 두 정수 값을 교환하는 함수를 작성하십시오.</summary>

```swift
var winner = "A"
func change(winner: inout String, to: String) {
    winner = to
}
print(winner)
change(winner: &winner, to: "Nat")
print(winner)
```
</details>


<details>
<summary>가드(guard) 문을 사용하여 옵셔널 문자열(String?)을 안전하게 래핑 해제하는 함수를 구현합니다.</summary>

```swift
func greet(person: [String: String]) {
    guard let name = person["name"] else { return }
    
    print("Hello, \(name)!")
    
    guard let location = person["location"] else {
        print("I hope the weather is nice near you.")
        return
    }
    print("I hope the weather is nice in \(location).")
}

greet(person: ["name" : "Nat"])
//Hello, Nat!
//I hope the weather is nice near you.
greet(person: ["name": "Nat", "location": "Cupertino"])
//Hello, Nat!
//I hope the weather is nice in Cupertino.
```
</details>


<details>
<summary>튜플을 입력으로 받아 두 요소의 합을 반환하는 함수를 만듭니다.</summary>

```swift
func operateTuples(_ inputTuples: (Int, Int)) -> Int {
    return inputTuples.0 + inputTuples.1
}
```
</details>


<details>
<summary>주어진 숫자의 팩토리얼을 계산하는 재귀 함수를 작성하십시오.</summary>

```swift
func isFactorial(_ num: Int) -> Int {
    let factorialNumber = num
    var result = 1
    for i in 1...factorialNumber {
        result *= i
    }
    return result
}

print(isFactorial(5))
```
</details>


<details>
<summary>Swift에서 print 기능의 적절한 사용법을 설명하십시오.</summary>

```swift
// 단순 문자열을 출력할 때는 print 를 사용하고, 인스턴스의 자세한 설명이 필요할 때는 dump 를 사용한다. 
// 문자열 보간법을 사용해 문자열 내 변수 또는 상수 실질적인 값을 표현하기 위해 사용
print(["cupertino": "LA", "gangNam": "Seoul"], 123, separator: "***", terminator: "\n")

// ["gangNam": "Seoul", "cupertino": "LA"]***123-

var num = 3.14
print("π: \(num)")
// π: 3.14
```
</details>


<details>
<summary>옵셔널 변수를 생성하고 옵셔널 바인딩을 사용하여 해당 값을 안전하게 언래핑하는 함수를 작성합니다.</summary>

```swift
//답변
```
</details>


<details>
<summary>옵셔널 정수(Int?)를 받아 2를 곱한 수(두배)를 반환하거나 입력이 nil인 경우 기본값을 반환하는 함수를 작성합니다.</summary>

```swift
//답변
```
</details>


<details>
<summary>정수 배열을 만들고 요소를 추가하고, 요소를 제거하고, 특정 인덱스에 있는 요소에 액세스하는 방법을 보여줍니다.</summary>

```swift
//답변
```
</details>


<details>
<summary>문자열 배열을 가져와 문자열(String)을 키로, 길이를 값으로 사용하여 딕셔너리를 반환하는 함수를 구현합니다.</summary>

```swift
//답변
```
</details>


<details>
<summary>정수 집합을 받아서 짝수만 포함하는 집합을 반환하는 함수를 작성하세요.</summary>

```swift
//답변
```
</details>


<details>
<summary>연관 값이 있는 열거형을 만들고 switch 문에서 사용하는 예제를 작성하세요.</summary>

```swift
//답변
```
</details>


<details>
<summary>원시 값으로 열거형을 구현하고 열거형 케이스의 원시 값에 접근하는 방법을 설명합니다.</summary>
- 원시값: 매칭되는 기본값(정수,문자열) 정해서 활용할 수 있다. 원시값을 입력안하면 자동으로 0, 1, 2 가 설정된다. 
아래 1을 처음으로 썼음으로 1부터 시작해서 7까지 원시값 호출 가능하고 호출은 아래 변수 `choiceDay` 처럼 쓰고 열거형 소괄호 rawValue 안에 정수형 숫자를 입력해 case 값을 불러온다.

```swift
enum Weekdays: Int {
    case mon = 1, tues, wed, thu, fri, sat, sun
}

var choiceDay = Weekdays(rawValue: 2)
```
</details>


<details>
<summary>옵셔널 정수(Int?)를 취하고 switch 문에서 옵셔널 패턴을 사용하여 nil인 경우와 nil이 아닌 경우를 모두 처리하는 함수를 작성하십시오.</summary>

```swift
//답변
```
</details>


<details>
<summary>열거형에서 unknown 키워드의 목적을 설명하십시오.</summary>

```swift
//답변
```
</details>



<details>
<summary>추가할 질문이 있다면 해당 양식 복사해서 붙여넣을 것!</summary>

```swift
//답변
```
</details>

