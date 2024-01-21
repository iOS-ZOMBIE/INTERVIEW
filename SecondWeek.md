# [iOS 🧟 ZOMBIE] iOS 인터뷰 - 2주차

스스로 설명할 수 있을 만큼의 인터뷰 능력을 기르는데 중점을 뒀습니다.

앨런29기 진도에 맞춰, 각 주차별로 준비한 인터뷰 문제를 풀어보고, 질문합니다.

<br>

<details>
<summary>두 개의 정수를 입력으로 받아 그 합을 반환하는 함수를 작성하십시오.</summary>

```swift
func addTwo(_ firstOne: Int, _ secondOne: Int) -> Int {
      return firstOne + secondOne
}
```
</details>


<details>
<summary>데이터는 RAM에 어떻게 저장됩니까?</summary>

```swift
//코드, 데이터, 힙, 스택으로 나뉘어 프로세스 형태로 올라간다.
//여기서 데이터 영역에서는 대표적으로 전역변수가 저장된다.
```
</details>


<details>
<summary>주어진 숫자의 제곱을 반환하는 함수를 작성하십시오.</summary>

```swift
 func multiplySec(_ num: Int) -> Int {
   return num * num
}
```
</details>


<details>
<summary>Swift에서 지역 범위와 전역 범위의 차이점을 설명하십시오.</summary>

```swift
지역범위는 함수 또는 어떠한 코드 블럭 안의 범위를 말하고, 지역 범위에서의 로컬 변수는 절대 외부에서 사용할 수 없다. 반면 전역 범위에서 선언된 전역 변수는 지역 범위 안쪽에서도 사용가능하다. 당연히 밖에서도 사용 가능하다. 
```
</details>


<details>
<summary>이름은 같지만 매개변수 유형이 다른 두 개의 함수를 만들어 함수 오버로딩을 구현하십시오.</summary>

```swift
func printSomething(_ num: Int){
 print(num)
}

func printSomething(_ str: String){
 print(str)
}
```
</details>


<details>
<summary>inout 매개변수를 사용하여 두 정수 값을 교환하는 함수를 작성하십시오.</summary>

```swift
func changeTwo(_ num1: inout Int, num2: inout Int) {
   let temp = num1
   num1 = num2
   num2 = temp
}
```
</details>


<details>
<summary>가드(guard) 문을 사용하여 옵셔널 문자열(String?)을 안전하게 래핑 해제하는 함수를 구현합니다.</summary>

```swift
func getOptionalValueString(_ str: String?) -> String {
  guard let str = str else { return }
  return str
}
```
</details>


<details>
<summary>튜플을 입력으로 받아 두 요소의 합을 반환하는 함수를 만듭니다.</summary>

```swift
 func addTupleElements(_ oneTuple: (Int,Int)) -> Int {
       return oneTuple.first + oneTuple.second
}
```
</details>


<details>
<summary>주어진 숫자의 팩토리얼을 계산하는 재귀 함수를 작성하십시오.</summary>

```swift
func fac(_ num: Int) -> Int {
  if num <= 1 {
    return 1
    }

   return num * fac(n-1)
}
```
</details>


<details>
<summary>Swift에서 print 기능의 적절한 사용법을 설명하십시오.</summary>

```swift
콘솔에 어떤 값을 문자열 형태로 출력하는데 사용된다.
```
</details>


<details>
<summary>옵셔널 변수를 생성하고 옵셔널 바인딩을 사용하여 해당 값을 안전하게 언래핑하는 함수를 작성합니다.</summary>

```swift
var str: String? = "thisisnotoptional"

func resolveOptional(_ str: String?) -> String {
  if let newstr = str {
   return newstr
  } else {
     print("ERROR: Optional failed")
     return "error"
   }

}
```
</details>


<details>
<summary>옵셔널 정수(Int?)를 받아 2를 곱한 수(두배)를 반환하거나 입력이 nil인 경우 기본값을 반환하는 함수를 작성합니다.</summary>

```swift

var n: Int? = 3

 func resolveOptionalandMulipleTwice(_ num: Int?, defaultNum: Int) -> Int {
   guard let num = num else {return defaultNum}
   return num * 2
}
```
</details>


<details>
<summary>정수 배열을 만들고 요소를 추가하고, 요소를 제거하고, 특정 인덱스에 있는 요소에 액세스하는 방법을 보여줍니다.</summary>

```swift
 var numarray = [Int]()
 numarray.append(4)
 numarray.append(3)
 numarray.remove(at: 1)
 var zeroElement = numarray[0]
 print(zeroElement)
```
</details>


<details>
<summary>문자열 배열을 가져와 문자열(String)을 키로, 길이를 값으로 사용하여 딕셔너리를 반환하는 함수를 구현합니다.</summary>

```swift
func getSTRLength(strarr: [String]) -> [String:Int] {
  var dic = [String: Int]()
  for str in strarr {
     dic[str] = str.count
  }
  return dic
}
```
</details>


<details>
<summary>정수 집합을 받아서 짝수만 포함하는 집합을 반환하는 함수를 작성하세요.</summary>

```swift
  func returnEvenNums(_ numarr: Set<Int>) -> Set<Int> {
   return numarr.filter { $0 % 2 == 0 }
   }
```
</details>


<details>
<summary>연관 값이 있는 열거형을 만들고 switch 문에서 사용하는 예제를 작성하세요.</summary>

```swift
 enum Animal {
  case dog(legCount: Int)
  case horse(legCount: Int)
  case cat(legCount: Int)
 }

 var myCatTom = Animal.cat(legCount: 4)

 switch myCatTom {
  case .dog(let leg):
    print("my tom's leg count : \(leg)")
  case .horse(let leg):
    print("my tom's leg count : \(leg)")
  case .cat(let leg):
    print("my tom's leg count : \(leg)")
 }
```
</details>


<details>
<summary>원시 값으로 열거형을 구현하고 열거형 케이스의 원시 값에 접근하는 방법을 설명합니다.</summary>

```swift
enum Bear: Int {
 case cass
 case terra
 case girin
 case kozel
}

let myBear = Bear.cass

print("\(myBear.type) 's is \(myBear.rawValue) score")
```
</details>


<details>
<summary>옵셔널 정수(Int?)를 취하고 switch 문에서 옵셔널 패턴을 사용하여 nil인 경우와 nil이 아닌 경우를 모두 처리하는 함수를 작성하십시오.</summary>

```swift
  func againOptional(_ num: Int?) {
   switch num {
    case .some(let value):
       print(value)
    case .none:
        print("nil")
   }
  }
```
</details>


<details>
<summary>열거형에서 unknown 키워드의 목적을 설명하십시오.</summary>

```swift
//만약 열거형이 계속 늘어날 수 있으면
//완전하지 않으니까 이후에 처리할 수도 있다는 걸 표시하려고!
```
</details>



<details>
<summary>추가할 질문이 있다면 해당 양식 복사해서 붙여넣을 것!</summary>

```swift
//답변
```
</details>

