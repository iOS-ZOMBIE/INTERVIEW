# [iOS 🧟 ZOMBIE] iOS 인터뷰 - 2주차

스스로 설명할 수 있을 만큼의 인터뷰 능력을 기르는데 중점을 뒀습니다.

앨런29기 진도에 맞춰, 각 주차별로 준비한 인터뷰 문제를 풀어보고, 질문합니다.

<br>

<details>
<summary>두 개의 정수를 입력으로 받아 그 합을 반환하는 함수를 작성하십시오.</summary>

```swift
func addNumbers(_ lhs: Int, _ rhs: Int) -> Int {
    return lhs + rhs
}
```
</details>


<details>
<summary>데이터는 RAM에 어떻게 저장됩니까?</summary>

```swift
// 데이터는 종류에 따라 RAM의 다른 분야에 저장됩니다. RAM의 코드영역에는 컴파일된 코드가, 데이터 영역에는 전역변수와 커스텀 타입, 힙 영역에는 클래스와 클로져, 마지막으로 스택영역에는 함수에 관한 데이터가 저장됩니다.
```
</details>


<details>
<summary>주어진 숫자의 제곱을 반환하는 함수를 작성하십시오.</summary>

```swift
// func powerOf(_ number: Int) -> Int {
    return number * number
}
```
</details>


<details>
<summary>Swift에서 지역 범위와 전역 범위의 차이점을 설명하십시오.</summary>

```swift
// 전역 범위는 코드 어디에서도 접근할 수 있는 범위인데 반해 지역 범위는 해당 지역 안 혹은 하위의 지역에서만 접근할 수 있습니다.
```
</details>


<details>
<summary>이름은 같지만 매개변수 유형이 다른 두 개의 함수를 만들어 함수 오버로딩을 구현하십시오.</summary>

```swift
func addThreeNumbers(_ num1: Int, _ num2: Int, _ num3: Int) -> Int {
    return num1 + num2 + num3
}

func addThreeNumbers(_ num1: Double, _ num2: Double, _ num3: Double) -> Double {
    return Double
}
```
</details>


<details>
<summary>inout 매개변수를 사용하여 두 정수 값을 교환하는 함수를 작성하십시오.</summary>

```swift
func swapNumbers(_ lhs: inout Int, _ rhs: inout Int) {
    let temp = lhs
    lhs = rhs
    rhs = temp
}
```
</details>


<details>
<summary>가드(guard) 문을 사용하여 옵셔널 문자열(String?)을 안전하게 래핑 해제하는 함수를 구현합니다.</summary>

```swift
// func unwrapOptionalString(_ wrappedStr: String?) -> String {
    guard let str = wrappedStr else { return "" }
    return str
}
```
</details>


<details>
<summary>튜플을 입력으로 받아 두 요소의 합을 반환하는 함수를 만듭니다.</summary>

```swift
func addTupleNumebrs(_ tuple: (Int, Int)) -> Int {
    return tuple.0 + tuple.1
}
```
</details>


<details>
<summary>주어진 숫자의 팩토리얼을 계산하는 재귀 함수를 작성하십시오.</summary>

```swift
func calculateFactorial(_ number: Int) -> Int {
    if number <= 1 {
        return 1
    }
    return calculateFactorial * calculateFatorial(number - 1)
}
```
</details>


<details>
<summary>Swift에서 print 기능의 적절한 사용법을 설명하십시오.</summary>

```swift
// print 함수는 입력한 String을 출력하는 함수입니다. 단순히 print안에 하나의 String을 써서 출력하는것 이외에도, 여러개의 String을 써도 출력가능하며, separator 파라미터에 String을 넣어서 여러개의 String이 들어왔을때 separator를 사이사이에 넣거나, terminator 파라미터를 이용해서 String의 가장끝에 원하는 String을 붙힐 수 있습니다.
```
</details>


<details>
<summary>옵셔널 변수를 생성하고 옵셔널 바인딩을 사용하여 해당 값을 안전하게 언래핑하는 함수를 작성합니다.</summary>

```swift
let notOptional: String? = "This is not Optional"
let someOptional: String = nil

func unwrapOptionalString(_ someString: String) -> String {
    guard let str = someString else { return "" }
    return str
}


```
</details>


<details>
<summary>옵셔널 정수(Int?)를 받아 2를 곱한 수(두배)를 반환하거나 입력이 nil인 경우 기본값을 반환하는 함수를 작성합니다.</summary>

```swift
func simpleCalculation(_ someNumber: Int?) -> Int {
    guard let number = someNumber else { return 0 }
    return someNumber * 2
}
```
</details>


<details>
<summary>정수 배열을 만들고 요소를 추가하고, 요소를 제거하고, 특정 인덱스에 있는 요소에 액세스하는 방법을 보여줍니다.</summary>

```swift

var intArray: [Int] = [0, 1] // 생성

intArray.append(2) // 추가
intArray.remove(at: 0) // 제거
print(intArray[0]) // 엑세스

```
</details>


<details>
<summary>문자열 배열을 가져와 문자열(String)을 키로, 길이를 값으로 사용하여 딕셔너리를 반환하는 함수를 구현합니다.</summary>

```swift
func makeStringDictionary(of strArray: [String]) -> [String: Int] {
    var resultDict: [String: Int] = [:]
    
    for elem in strArray {
        resultDict.updateValue(elem.count, forKey: elem)
    }
    
    return resultDict
}

let strArr: [String] = ["가", "나다", "라마바", "사아자차"]
print(makeStringDictionary(of: strArr))

```
</details>


<details>
<summary>정수 집합을 받아서 짝수만 포함하는 집합을 반환하는 함수를 작성하세요.</summary>

```swift
func filterOddNumber(of intSet: Set<Int>) -> Set<Int> {
    var resultSet: Set<Int> = Set<Int>()
    
    for elem in intSet {
        if elem % 2 == 0 {
            resultSet.insert(elem)
        }
    }
    
    return resultSet
}

let inputSet: Set<Int> = Set([1, 2, 3, 4, 5, 6, 7, 8])
print(filterOddNumber(of: inputSet))

print(inputSet.filter({$0 % 2 == 0})) // 흠... 이것도 되넹
```
</details>


<details>
<summary>연관 값이 있는 열거형을 만들고 switch 문에서 사용하는 예제를 작성하세요.</summary>

```swift
// 추후 질문하기
enum NetworkResponse {
    case respose(code: ResponseCases)
}

enum ResponseCases: Int {
    case success = 200
    case serverError = 400
    case clientError = 500
}

let networkResponse: NetworkResponse = .respose(code: .success)

switch networkResponse {
case .respose(code: .success):
    print("SUCCESS")
case .respose(code: .clientError):
    print("CLIENT ERROR")
case .respose(code: .serverError):
    print("SERVER ERROR")
}
```
</details>


<details>
<summary>원시 값으로 열거형을 구현하고 열거형 케이스의 원시 값에 접근하는 방법을 설명합니다.</summary>

```swift
enum SomeEnum: String {
case first = "First"
case second = "Second"
case third = "Third"
}

let someEnum: SomeEnum  = .first

print(someEnum.rawValue)
```
</details>


<details>
<summary>옵셔널 정수(Int?)를 취하고 switch 문에서 옵셔널 패턴을 사용하여 nil인 경우와 nil이 아닌 경우를 모두 처리하는 함수를 작성하십시오.</summary>

```swift
func unwrapInt(of someNumber: Int?) -> Int {
    switch someNumber {
    case let .some(x):
        return x
    case .none:
        return 0
    }
}


let someNumber = 2
let otherNumber: Int? = nil
print(unwrapInt(of: someNumber))
print(unwrapInt(of: otherNumber))
```
</details>


<details>
<summary>열거형에서 unknown 키워드의 목적을 설명하십시오.</summary>

```swift
// switch의 case에서 모든 열거형의 case를 처리하지 못하고 default문으로 처리하는 경우가 있는경우 warning을 사용자에게 줍니다. 예를 들어 초기 코드에서는 case가 first, second, third가 있었고 switch문에서 default가 아니라 모든 case로 이 값들을 처리하고 있었다고 가정하겠습니다. 그런데 추후에 네번째 케이스인 fourth가 생겼다고 하면 만약 이전 switch 문에서 이 fourth문을 처리하지 않고 default문으로 처리하는 상황이 발생하면 @unknown 어트리뷰트를 default 앞에 붙혀놓는다면 warning이 발생해서 미처 처리하지 못한 case에 대한 대처를 할 수 있습니다.
```
</details>



<details>
<summary>추가할 질문이 있다면 해당 양식 복사해서 붙여넣을 것!</summary>

```swift
//답변
```
</details>

