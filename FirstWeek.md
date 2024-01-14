# [iOS 🧟 ZOMBIE] iOS 인터뷰 - 1주차

스스로 설명할 수 있을 만큼의 인터뷰 능력을 기르는데 중점을 뒀습니다.

앨런29기 진도에 맞춰, 각 주차별로 준비한 인터뷰 문제를 풀어보고, 질문합니다.

<br>

<details>
<summary>컴퓨터 시스템에서 CPU의 주요 기능은 무엇입니까?</summary>

 - 연산: 데이터 조작 및 계산하는 등의 작업
 - 제어: CPU 프로그램 실행 흐름 제어
 - 기억장치 관리: CPU는 주기억장치(RAM)에서 데이터 명령어를 읽고 쓰며, 프로그램 작업에 필요한 정보를 저장 검색함.
 - 입출력처리(input/output processing): CPU는 외부장치와의 상호작용을 통해 데이터를 입력받고 출력한다.
 - 인터럽트 처리
 - 레지스터 관리
 - 명령어 처리

</details>


<details>
<summary>데이터는 RAM에 어떻게 저장됩니까?</summary>

```swift
1. 프로그램 실행 
-> 2.변수 및 데이터 구조 정의 후 메모리 할당(프로그램이 실행되는 동안 필요한 데이터 저장)
 -> 3. 메모리 주소 할당: 각 변수,데이터 구조는 메모리 상 고유한 메모리 주소를 가진다. 이 주소를 이용해 프로그램은 데이터에 접근하고 조작한다. 
 -> 4. 데이터 쓰기 및 읽기: 프로그램이 실행되는 동안 데이터는 메모리에 쓰여지거나 읽혀진다. CPU는 명령어를 통해 메모리 주소에 접근하고 데이터를 읽거나 쓸 수 있다. 
 -> 5. 임시 데이터(스택): 함수 호출과 같은 작업 중 발생하는 임시 데이터 함수 호출 정보는 스택 메모리에 저장한다. 함수 호출과 반환에 따라 데이터를 추가하거나 제거한다. 
 -> 6. 동적할당: 프로그램 실행 중 동적으로 메모리를 할당할 때에는 주로 heap 메모리를 사용한다. 동적할당은 프로그램이 실행 중에 필요에 따라 메모리를 동적으로 할당하고 해제하는 것을 말한다. 
중요한 점: 데이터가 RAM에 저장되면, CPU가 데이터에 빠르게 액세스해 처리가능 
단, RAM 은 휘발성 메모리라서 전원이 꺼지면 저장된 데이터 사라지지만, 빠르게 데이터를 읽고 쓰는게 가능해 데이터 처리에 효과적이다.
```
</details>


<details>
<summary>음수는 2의 보수를 사용하여 메모리에 어떻게 표시됩니까?</summary>

```swift
//  음수는 이진수 표현에서 모든 비트를 반전한 다음 1을 더하여 얻은 2의 보수를 사용하여 메모리에 표현됩니다.
```
</details>


<details>
<summary>Swift에서 플레이그라운드의 목적은 무엇입니까?</summary>

```swift
//답변
```
</details>


<details>
<summary>프로그래밍 언어에서 등호(=)는 무엇을 나타냅니까?</summary>

```swift
//답변
```
</details>


<details>
<summary>프로그래밍에서 일반적으로 사용되는 세 가지 특수 문자를 말하십시오.</summary>

```swift
//답변
```
</details>


<details>
<summary>프로그래밍에서 경고와 오류의 차이점은 무엇입니까?</summary>

```swift
//답변
```
</details>


<details>
<summary>Swift의 기본 산술 연산자는 무엇입니까?</summary>

```swift
//답변
```
</details>


<details>
<summary>산술 연산의 우선 순위는 무엇입니까?</summary>

```swift
//답변
```
</details>


<details>
<summary>Swift의 if-else 문에 대해 설명하세요.</summary>

```swift
//답변
```
</details>


<details>
<summary>Swift에서 switch 문은 어떻게 작동합니까?</summary>

```swift
//답변
```
</details>


<details>
<summary>패턴 매칭과 함께 switch 문을 사용하는 예를 제시하십시오.</summary>

```swift
//답변
```
</details>


<details>
<summary>Swift에서 튜플의 기본 사항을 설명하십시오.</summary>

```swift
//답변
```
</details>


<details>
<summary>Swift 함수에서 튜플을 어떻게 사용할 수 있습니까?</summary>

```swift
//답변
```
</details>


<details>
<summary>컴퓨터 시스템에서 CPU의 주요 기능은 무엇입니까?</summary>

```swift
//답변
```
</details>


<details>
<summary>Swift에서 삼항 연산자의 예를 작성하십시오.</summary>

```swift
let contentHeight = 40
let hasHeader = true
let rowHeight = contentHeight + (hasHeader ? 50 : 20)
// rowHeight is equal to 90
```
</details>


<details>
<summary> Swift의 폐쇄 범위 연산자와 반개방 범위 연산자의 차이점을 설명하십시오. </summary>

```swift
//답변
```
</details>


<details>
<summary>Swift에서 for-in 루프를 어떻게 생성합니까?</summary>

```swift
//답변
```
</details>


<details>
<summary>Swift에서 while 루프와 반복-while 루프의 차이점은 무엇입니까?</summary>

```swift
//답변
```
</details>


<details>
<summary>루프에서 continue 및 break 문을 사용해야 하는 경우는 언제입니까?</summary>

```swift
//답변
```
</details>


<details>
<summary>두 숫자의 곱셈을 계산하는 함수를 작성하십시오.</summary>

```swift
func multiplyTwoNums(_ param1: Int, _ param2: Int) -> Int {
    return param1 * param2
}
```
</details>


<details>
<summary>Swift에서 함수의 기본 개념을 설명하십시오.</summary>

```swift
/* 
함수는 특별한 업무를 수행하는 자립적인 코드 덩어리다. 프로그래머는 함수에 그것이 무엇을 하는지 알아보는 이름을 지어줄 수 있다. 그리고 그 이름은 필요한 업무를 수행하기 위해 (함수를) 호출할 때 사용한다. 
*/
func 함수이름(매개변수) -> 반환 값(값의 타입) {
	실행할 코드 (함수 구현부)
	return 반환 값(의 타입)
}
```
</details>


<details>
<summary>추가할 질문이 있다면 해당 양식 복사해서 붙여넣을 것!</summary>

```swift
//답변
```
</details>

