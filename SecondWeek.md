# [iOS 🧟 ZOMBIE] iOS 인터뷰 - 2주차

스스로 설명할 수 있을 만큼의 인터뷰 능력을 기르는데 중점을 뒀습니다.

앨런29기 진도에 맞춰, 각 주차별로 준비한 인터뷰 문제를 풀어보고, 질문합니다.

<br>

<details>
<summary>두 개의 정수를 입력으로 받아 그 합을 반환하는 함수를 작성하십시오.</summary>

```swift
//답변
func intSum(_ num1: Int, _ num2: Int) -> Int {
    return num1 + num2
}
```
</details>


<details>
<summary>데이터는 RAM에 어떻게 저장됩니까?</summary>

```swift
//답변
데이터는 RAM에서 코드, 데이터, 힙, 스택 영역으로 나뉘어 저장된다.
코드(프로그램) 영역에는 프로그램의 명령어(코드)가 저장되고, 데이터 영역에는 전역변수와,
타입(static/class) 변수가 공통으로 공유되기 위해 저장된다.
힙 영역에는 일반적으로 긴 시간 저장하는, 크고 관리해야할 필요가 있는 데이터를 저장하며,
스택 영역은 함수 실행을 위한 임시적 공간으로 크기가 작고 빠르게 사용해야 하는 데이터를 저장한다.
이처럼 RAM은 데이터의 종류에 따라 최대의 속도와 최적의 조건으로 사용하기 위한 메모리 구조를 가지고 있다.
```
</details>


<details>
<summary>주어진 숫자의 제곱을 반환하는 함수를 작성하십시오.</summary>

```swift
//답변
주어진 숫자를 정수로 가정하였을 때

func squared(of number: Int) -> Int {
    return number * number
}
```
</details>


<details>
<summary>Swift에서 지역 범위와 전역 범위의 차이점을 설명하십시오.</summary>

```swift
//답변
지역 범위란, 현재 위치와 가장 가까운 중괄호 {} 내부를 말하며, 전역 범위는 그 외 바깥의 전체적인 범위를 말한다.
```
</details>


<details>
<summary>이름은 같지만 매개변수 유형이 다른 두 개의 함수를 만들어 함수 오버로딩을 구현하십시오.</summary>

```swift
//답변
두 숫자의 평균을 구하는 함수

- 정수
func average(intNum1: Int, intNum2: Int) -> Int {
    return (intNum1 + intNum2) / 2
}

- 실수
func average(doubleNum1: Double, doubleNum2: Double) -> Double {
    return (doubleNum1 + doubleNum2) / 2
}
```
</details>


<details>
<summary>inout 매개변수를 사용하여 두 정수 값을 교환하는 함수를 작성하십시오.</summary>

```swift
//답변
func change(num1: inout Int, num2: inout Int) {
    let temp = num1
    num1 = num2
    num2 = temp
}
```
</details>


<details>
<summary>가드(guard) 문을 사용하여 옵셔널 문자열(String?)을 안전하게 래핑 해제하는 함수를 구현합니다.</summary>

```swift
//답변
옵셔널 문자열이 언래핑 된 문자열이 반환되고, nil의 경우 빈 문자열을 반환한다는 가정 하에

func unwrapping(_ str: String?) -> String {
    guard let unwrappedStr = str else { return "" }
    return unwrappedStr
}
```
</details>


<details>
<summary>튜플을 입력으로 받아 두 요소의 합을 반환하는 함수를 만듭니다.</summary>

```swift
//답변
튜플 내의 두 요소가 정수라는 전제 하에

func summary(nums: (Int, Int)) -> Int {
    return nums.0 + nums.1
}
```
</details>


<details>
<summary>주어진 숫자의 팩토리얼을 계산하는 재귀 함수를 작성하십시오.</summary>

```swift
//답변
func factorial(_ num: Int) -> Int {
    if num < 2 {
        return 1
    }
    
    return num * factorial(num - 1)
}
```
</details>


<details>
<summary>Swift에서 print 기능의 적절한 사용법을 설명하십시오.</summary>

```swift
//답변
콘솔에 출력하거나 개발자의 디버깅용으로 주로 사용된다.
```
</details>


<details>
<summary>옵셔널 변수를 생성하고 옵셔널 바인딩을 사용하여 해당 값을 안전하게 언래핑하는 함수를 작성합니다.</summary>

```swift
//답변
var str: String? = "박광배"

func unwrapping(_ str: String?) -> String {
    guard let unwrappedStr = str else { return "" }
    return unwrappedStr
}
```
</details>


<details>
<summary>옵셔널 정수(Int?)를 받아 2를 곱한 수(두배)를 반환하거나 입력이 nil인 경우 기본값을 반환하는 함수를 작성합니다.</summary>

```swift
//답변
func multipleTwo(_ num: Int?) -> Int {
    guard let unwrappedNum = num else { return 0 }

    return unwrappedNum * 2
}
```
</details>


<details>
<summary>정수 배열을 만들고 요소를 추가하고, 요소를 제거하고, 특정 인덱스에 있는 요소에 액세스하는 방법을 보여줍니다.</summary>

```swift
//답변
var nums = [1, 2, 3, 4, 5, 6, 7]

- 요소 추가
nums.append(8)

- 특정 인덱스 요소 엑세스
nums[1]

- 요소 제거
nums.removeFirst()
nums.removeLast()
nums.popLast()
nums.removeAll()
```
</details>


<details>
<summary>문자열 배열을 가져와 문자열(String)을 키로, 길이를 값으로 사용하여 딕셔너리를 반환하는 함수를 구현합니다.</summary>

```swift
//답변

func makeDic(str: [String]) -> Dictionary<String, Int> {
    var strKey = ""

    for i in str {
        strKey += i
    }

    return [strKey: str.count]
}
```
</details>


<details>
<summary>정수 집합을 받아서 짝수만 포함하는 집합을 반환하는 함수를 작성하세요.</summary>

```swift
//답변

func pickEvenNums(in nums: Set<Int>) -> Set<Int> {
    var resultArr: Set<Int> = []

    for num in nums {
        if num % 2 == 0 {
            resultArr.insert(num)
        }
    }

    return resultArr
}
```
</details>


<details>
<summary>연관 값이 있는 열거형을 만들고 switch 문에서 사용하는 예제를 작성하세요.</summary>

```swift
//답변

enum Week {
    case weekday
    case weekend
}

let monday = Week.weekday

switch monday {
    case .weekday:
        print("평일")
    case .weekend:
        print("주말")
}
```
</details>


<details>
<summary>원시 값으로 열거형을 구현하고 열거형 케이스의 원시 값에 접근하는 방법을 설명합니다.</summary>

```swift
//답변
enum Weekend: String {
    case saturday = "토"
    case sunday = "일"
}

- 원시값에 접근하기 위해서는 case 뒤에 rawValue라는 키워드를 붙여주면 된다.
Weekend.saturday.rawValue
```
</details>


<details>
<summary>옵셔널 정수(Int?)를 취하고 switch 문에서 옵셔널 패턴을 사용하여 nil인 경우와 nil이 아닌 경우를 모두 처리하는 함수를 작성하십시오.</summary>

```swift
//답변

switch optNumber {
    case .some(let num):
        print(num)
    case .none:
         print("nil")
}
```
</details>


<details>
<summary>열거형에서 unknown 키워드의 목적을 설명하십시오.</summary>

```swift
//답변
열거형의 모든 케이스를 다룰 수 있도록 돕는 것이 목적이다.
switch문에서 default 앞에 unknown 키워드를 붙이는 경우 열거형의 모든 케이스를 다루는 지 확인할 수 있다.
```
</details>
