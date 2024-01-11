# [iOS 🧟 ZOMBIE] iOS 인터뷰 - 1주차

스스로 설명할 수 있을 만큼의 인터뷰 능력을 기르는데 중점을 뒀습니다.

앨런29기 진도에 맞춰, 각 주차별로 준비한 인터뷰 문제를 풀어보고, 질문합니다.

<br>

<details>
<summary>컴퓨터 시스템에서 CPU의 주요 기능은 무엇입니까?</summary>

```swift
// 멀티 코어를 활용한 연산 처리, 강의에서는 instruction 처리를 주로 다루었다.
```
</details>


<details>
<summary>데이터는 RAM에 어떻게 저장됩니까?</summary>

```swift
// 메인메모리에 프로그램이 실행 중일 때 프로세스 단위로 올라가는데, 프로세스는 맨 위에서 아래로 내려오는 stack, 그 밑에서 올라오는 heap, 전역변수 등이 저장되는 data(물론 글로벌이라고 해도 초기화 여부에 따라 영역이 나뉜다),
// 그리고 작성한 코드가 작성되는 코드 영역으로 나뉘어 저장된다. 모든 데이터는 이진 형태로 기록된다. 
```
</details>


<details>
<summary>음수는 2의 보수를 사용하여 메모리에 어떻게 표시됩니까?</summary>

```swift
//뭔가 질문이 이상한데 질문 속에 답이 있다. 음수는 2의 보수를 사용해서 메모리에 표시된다. 2의 보수를 다시 취하고 +1을 하면 원래 수로 바뀐다.
```
</details>


<details>
<summary>Swift에서 플레이그라운드의 목적은 무엇입니까?</summary>

```swift
//스위프트의 문법 구조를 갖고 놀 수 있게 해준다.
```
</details>


<details>
<summary>프로그래밍 언어에서 등호(=)는 무엇을 나타냅니까?</summary>

```swift
// 대입연산자이다.
```
</details>


<details>
<summary>프로그래밍에서 일반적으로 사용되는 세 가지 특수 문자를 말하십시오.</summary>

```swift
// () {} , 등이 있다.
```
</details>


<details>
<summary>Swift에서 변수와 상수의 차이점은 무엇입니까?</summary>

```swift
//변수는 값을 변경할 수 있고, 상수는 초기화 후 값을 변경할 수 없다.
```
</details>



<details>
<summary>Swift에서 타입 추론의 개념을 설명하세요.</summary>

```swift
//따로 타입 추론을 하지 않아도, 초기화 시 대입한 해당 값을 기반으로 컴파일러가 알아서 타입을 추측하는 것
```
</details>



<details>
<summary>Swift의 은 타입 앨리어스(Type Alias)는 무엇이며 왜 사용해야 합니까?</summary>

```swift
//일종의 별칭
typealias Name = String
var alfieName : Name = "Alfie"
// 사용 이유는 클래스나 구조체같은 자체적 타입을 만들 때 주로 사용된다.
```
</details>



<details>
<summary>프로그래밍에서 경고와 오류의 차이점은 무엇입니까?</summary>

```swift
//경고는 말 그대로 경고, 시뮬레이터 실행 시 앱이 꺼지지는 않는다(거의)
// 하지만 에러는 반드시 꺼진다
```
</details>


<details>
<summary>Swift의 기본 산술 연산자는 무엇입니까?</summary>

```swift
// +, -, *, /가 포함된다.
```
</details>


<details>
<summary>산술 연산의 우선 순위는 무엇입니까?</summary>

```swift
//그냥 괄호 잘 사용해라
```
</details>


<details>
<summary>Swift의 if-else 문에 대해 설명하세요.</summary>

```swift
// 이거 아니면 저거해라라는 식의 조건문이다.
if true {
} else {
}
```
</details>


<details>
<summary>Swift에서 switch 문은 어떻게 작동합니까?</summary>

```swift
//switch 옆에 사용된 변수를 기반으로, 위에서 아래로 하나하나 대응해가며 실행된다. 그래서 중복 답이 여러개면 꼭 의도에 따라 break를 적절히 써줘야한다. fallthrough도 마찬가지...
```
</details>


<details>
<summary>패턴 매칭과 함께 switch 문을 사용하는 예를 제시하십시오.</summary>

```swift
// ~= 얘가 패턴매칭
let testScore = 50
if 90...100 ~= testScore {
   print("A+")
} else if 80...89 ~= testScore {
   print("A")
} else if 70...79 ~= testScore {
   print("B+")
} else {
   print("공부를 안했구나 너")
}
```
</details>


<details>
<summary>Swift에서 튜플의 기본 사항을 설명하십시오.</summary>

```swift
// 값을 괄호로 묶어 저장할 수 있는 복합적 유형이다. 
```
</details>


<details>
<summary>Swift 함수에서 튜플을 어떻게 사용할 수 있습니까?</summary>

```swift
//리턴 값이 여러개일 때 한꺼번에 리턴할 수 있다.
```
</details>


<details>
<summary>Swift에서 삼항 연산자의 예를 작성하십시오.</summary>

```swift
 let winner = (jon > bob) ? "jon 우승" : "bob 우승"
```
</details>



<details>
<summary> Swift의 폐쇄 범위 연산자와 반개방 범위 연산자의 차이점을 설명하십시오. </summary>

```swift
//폐쇄 범위 연산자는 양쪽 경계값 모두 포함, 반개방은 오른쪽은 제외
```
</details>


<details>
<summary>Swift에서 for-in 루프를 어떻게 생성합니까?</summary>

```swift
for i in 0..<arr.count {
  print(arr[i])
}
```
</details>


<details>
<summary>Swift에서 while 루프와 반복-while 루프의 차이점은 무엇입니까?</summary>

```swift
//repeat-while은 한 번 실행하고 들어간다.즉 무조건 한 번 이상은 실행되는 것!
```
</details>


<details>
<summary>루프에서 continue 및 break 문을 사용해야 하는 경우는 언제입니까?</summary>

```swift
// continue는 다음 반복으로 넘길 때, break는 가장 가까운 반복문을 빠져나갈 때
```
</details>


<details>
<summary>두 숫자의 곱셈을 계산하는 함수를 작성하십시오.</summary>

```swift
func multiply(_ firstNum: Int, _ secondNum: Int){
   return firstNum * secondNum
}
```
</details>


<details>
<summary>Swift에서 함수의 기본 개념을 설명하십시오.</summary>

```swift
// input을 넣으면 output이 나오는 매직박스
// 다양한 instruction을 합쳐놓은 일종의 shortcut
// 리턴값을 Void로 설정해 없앨 수도 있다.
```
</details>


<details>
<summary>추가할 질문이 있다면 해당 양식 복사해서 붙여넣을 것!</summary>

```swift
//답변
```
</details>

