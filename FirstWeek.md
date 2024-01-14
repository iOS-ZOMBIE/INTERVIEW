# [iOS 🧟 ZOMBIE] iOS 인터뷰 - 1주차

스스로 설명할 수 있을 만큼의 인터뷰 능력을 기르는데 중점을 뒀습니다.

앨런29기 진도에 맞춰, 각 주차별로 준비한 인터뷰 문제를 풀어보고, 질문합니다.

<br>

<details>
<summary>컴퓨터 시스템에서 CPU의 주요 기능은 무엇입니까?</summary>

```swift
// 연산을 하는것입니다. 크게는 산술적인 연산인 덧셈, 뺄셈등을 하는것이지만, 자세히 들여다보면 메모리에서 값 읽어들이기, 읽어들인값 연산, 저장 등  
```
</details>

<detail>
<summary> (꼬리질문) CPU와 GPU의 차이는 무엇입니까? </summary>

```swift
// 
```
</detail>

<details>
<summary>데이터는 RAM에 어떻게 저장됩니까?</summary>

```swift
// 어떤 데이터냐에 따라 답변이 달라질것 같습니다. Swift의 코드같은 경우에는 프로그램으로 하드디스크에 저장되어있다가 실행을 시켜서 프로세스가 되면서 컴파일러가 컴파일을 통해 어셈블리어로 변환하여 메모리의 코드 영역에 올라가게 됩니다. 프로그램을 실행하면서 발생하는 전역변수는 RAM의 데이터 영역에 저장되며, 함수나 반복문을 돌면서 만들어지는 변수들은 스택영역에 저장됩니다. 마지막으로 클래스의 인스턴스는 힙에 저장됩니다.
```
</details>


<details>
<summary>음수는 2의 보수를 사용하여 메모리에 어떻게 표시됩니까?</summary>

```swift
//답변
```
</details>


<details>
<summary>Swift에서 플레이그라운드의 목적은 무엇입니까?</summary>

```swift
// 간단하게 여러가지를 만들어보기 위함입니다. 간단한 Swift 문법이라던가 아주 작은 앱 같은 경우는 플레이그라운드로 시험삼아서 만들어볼 수 있습니다.
```
</details>


<details>
<summary>프로그래밍 언어에서 등호(=)는 무엇을 나타냅니까?</summary>

```swift
// 할당을 나타냅니다. 실생활에서 등호는 '같다'라는 의미를 나타내는데에 반해 프로그래밍언어에서는 우측에 있는 값을 좌측의 변수 혹은 상수의 메모리값에 넣는 할당의 역할을 합니다.
```
</details>


<details>
<summary>프로그래밍에서 일반적으로 사용되는 세 가지 특수 문자를 말하십시오.</summary>

```swift
// | 파이프 & 앰퍼센드 ! 익스클레메이션 마크
```
</details>


<details>
<summary>프로그래밍에서 경고와 오류의 차이점은 무엇입니까?</summary>

```swift
// 프로그램이 멈추느냐 아니냐로 차이점을 말할 수 있겠습니다. 경고는 프로그램을 정지시키지는 않지만 추후에 문제가 될 수 있는 부분들을 컴파일러가 지적해주는것이라면, 오류는 그대로 실행시킨다면 앱이 켜지지 않거나 꺼질정도의 큰 문제를 컴파일러가 지적해주는것입니다. 따라서 오류는 반드시 고쳐야하는 문제입니다.
```
</details>


<details>
<summary>Swift의 기본 산술 연산자는 무엇입니까?</summary>

```swift
// Swift는 모든 숫자 타입에 대해 +, -, *, / 4개의 기본 산술연산자를 제공합니다.
```
</details>


<details>
<summary>산술 연산의 우선 순위는 무엇입니까?</summary>

```swift
// 실생활에서와 같이 괄호가 가장 우선적이며, 그 이후로 곱셈과 나눗셈의 우선 순위가 같고, 마지막으로 덧셈과 뺄셈의 우선순위가 같습니다.
```
</details>


<details>
<summary>Swift의 if-else 문에 대해 설명하세요.</summary>

```swift
// if-else 문은 코드에 분기처리를 할 수 있게 해주는 방법중에 하나입니다. 여기서 분기처리란 if 라는 키워드 뒤에 붙는 조건무의 결과인 참, 거짓에 따라 특정한 코드를 실행시킬 수 있게 해주는것이 if-else문입니다.
```
</details>


<details>
<summary>Swift에서 switch 문은 어떻게 작동합니까?</summary>

```swift
// Switch문 또한 이전에 설명한 if-else문과 같이 분기처리를 할 수 있게 해주는것입니다. if else문은 조건문에 따라 참 거짓의 컴파일된 코드로 점프를 하지만, switch 문은 컴파일될떄 Switch table을 생성하여 Switch문의 키 값에 해당하는 값의 case로 점프를 합니다.
```
</details>


<details>
<summary>패턴 매칭과 함께 switch 문을 사용하는 예를 제시하십시오.</summary>

```swift
// Swift는 다양한 문법적인 패턴으로 개발자의 개발을 돕습니다. 가장 먼저 생각나는것은 wild card 패턴으로 사용하지 않을 변수는 이름을 _로 만들어서 사용하지 않는다고 컴파일러에게 알릴 수 있습니다. 다른 패턴매칭 중 하나는 value binding 패턴으로 매칭되는 값을 변수 혹은 상수에 할당하는 패턴으로 let 혹은 var 키워드를 이용합니다.
```
</details>


<details>
<summary>Swift에서 튜플의 기본 사항을 설명하십시오.</summary>

```swift
// 튜플은 다양한 타입을 한번에 담을 수 있는 Swift의 타입 중 하나입니다. 
```
</details>


<details>
<summary>Swift 함수에서 튜플을 어떻게 사용할 수 있습니까?</summary>

```swift
// 다양한 값을 묶어서 리턴값을 반환할때 사용할 수 있습니다. Swift에서 함수는 하나의 값만 반환할 수 있는데 만약 여러가지 값을 반환하려고 한다면 튜플을 이용해서 하나의 튜플로 묶어서 반환할 수 있습니다.
```
</details>


<details>
<summary>컴퓨터 시스템에서 CPU의 주요 기능은 무엇입니까?</summary>

```swift
// ?? 질문을 이해 못함
```
</details>


<details>
<summary>Swift에서 삼항 연산자의 예를 작성하십시오.</summary>

```swift
// if else 문과 동일하게 사용할 수 있습니다. 조건문 : 참일떄의 값 혹은 코드 ? 거짓일때의 값 혹은 코드를 조금 더 간단하고 가독성 좋게 쓸 수 있습니다.
```
</details>


<details>
<summary> Swift의 폐쇄 범위 연산자와 반개방 범위 연산자의 차이점을 설명하십시오. </summary>

```swift
// 범위의 끝을 포함하느냐 아니냐로 차이점을 말할 수 있을것 같습니다. 폐쇄범위 연산자는 양쪽 끝 값을 전부 다 포함하지만 반개방 범위 연산자는 한쪽 끝 값은 포함하는데 한쪽 끝 값은 포함하지 않습니다.
```
</details>


<details>
<summary>Swift에서 for-in 루프를 어떻게 생성합니까?</summary>

```swift
// for문은 in 키워드 뒤에 붙는 범위 값으로 중괄호 안의 코드를 반복해서 사용하는 반복문입니다. for 변수 혹은 상수 in 범위 {...}의 방법으로 생성합니다. 컴파일된 코드 레벨에서 본다면 점프를 이용해서 루프를 빠져나가게 해주느느냐 아니냐를 파악하여 코드를 반복시켜줍니다. 
```
</details>


<details>
<summary>Swift에서 while 루프와 반복-while 루프의 차이점은 무엇입니까?</summary>

```swift
// 코드를 가장 처음 한번은 실행시키냐 아니냐의 차이가 있습니다. repeat-while문 같은 경우 최초 1회는 코드가 무조건 작동하고 while 키워드 뒤의 조건에 따라 추후에 반복을 할지 아닐지를 결정하지만, while문은 조건에 따라 코드를 한번도 동작하지 않고 그냥 넘어갈 수 도 있습니다.
```
</details>


<details>
<summary>루프에서 continue 및 break 문을 사용해야 하는 경우는 언제입니까?</summary>

```swift
// 특정 상황에서 반복의 흐름에 제어를 해주고 싶을때 사용합니다. 루프는 일반적으로는 주어진 횟수 혹은 초기에 주어진 조건만큼 계속해서 반복하지만, 만약 실행 도중에 어떤 상황에서 흐름을 벗어나거나, 해당 코드를 실행시키고 싶지 않을때 continue 혹은 break 문을 사용합니다.

```
</details>


<details>
<summary>두 숫자의 곱셈을 계산하는 함수를 작성하십시오.</summary>

```swift
// 두 숫자가 어떤 타입인지 몰라서 이렇게 작성함
func multiply<T: Numeric>(_ lhs: T, _ rhs: T) -> T {
    return lhs * rhs
}
// Numeric protocol: numeric 프로토콜은 기본 산술연산자와 변형된 연산자들에 대한 편의성을 제공해줍니다 
```
</details>


<details>
<summary>Swift에서 함수의 기본 개념을 설명하십시오.</summary>

```swift
// 함수란 기본적으로는 어떤 입력값을 받았을때 내부적인 로직을 처리해서 출력값을 반환하는것입니다. 
```
</details>


<details>
<summary>추가할 질문이 있다면 해당 양식 복사해서 붙여넣을 것!</summary>

```swift
//넹
```
</details>

