# [iOS 🧟 ZOMBIE] iOS 인터뷰 - 3주차

스스로 설명할 수 있을 만큼의 인터뷰 능력을 기르는데 중점을 뒀습니다.

앨런29기 진도에 맞춰, 각 주차별로 준비한 인터뷰 문제를 풀어보고, 질문합니다.

<br>

<details>
<summary>스위프트에서 클래스와 구조체의 차이점을 설명합니다.</summary>

```swift
//클래스의 인스턴스는 참조타입, 구조체는 값타입
//각자 인스턴스는 각각 힙과 스택에 할당된다.
// 빠르기는 당연히 참조가 아닌 구조체가 빠르다.
```
</details>

<details>
<summary>클래스(참조 유형)와 구조체(값 유형) 간의 메모리 관리 차이를 설명합니다.(인스턴스의 복사와 관련하여 설명할것)</summary>

```swift
//위에서 다 썼는데...
//데이터 영역에 frame이 있다. 
```
</details>


<details>
<summary>구조체의 상수 인스턴스를 선언하는 방법을 보여주고 속성이 변경되었을 때 그 동작을 설명합니다.</summary>

```swift
//let으로 구조체의 인스턴스를 선언하면 해당 속성을 변경할 수 없다.
//but 클래스는 참조라 가능!
struct T1 {
  var faker = 99999
}

let T1 = T1()
//T1.faker = 99 이러면 에러난다고!
//
```
</details>


<details>
<summary>스위프트에서 초기화의 의미에 대해 설명합니다.</summary>

```swift
//속성에 초기값, 디폴트값을 할당해서 클래스 또는 구조체의 요소를 설정하는 것
// init 생성자로 보통 이루어진다
// 아무것도 안건들면 클래스는 기본 생성자, 구조체는 기본 생성자 + 멤버와이즈 생성자가 자동으로 들어간다.
```
</details>


<details>
<summary>클래스와 구조체의 초기화 과정을 비교해서 설명합니다.</summary>

```swift
//생성자로 인스턴스를 만들었다!
// 클래스는 인스턴스를 생성한 변수에 힙 인스턴스 주소가 담기고, 따라가보면 힙에서도 데이터 영역의 frame을 가리키고 있다.
// 생성자 함수에서 정의했듯이, 생성자 함수 콜을 만나면 코드 영역에서 힙으로 인스턴스 변수에 담긴 주소를 타고 넘어가면, 해당 힙에서 변수들을 생성자에서 정의한대로 초기화한다.
//but 구조체 같은 경우 코드 영역에서 생성자를 콜해서 생성자가 스택에 쌓이면, 여기서 바로 프로퍼티에 초기화가 일어난다. 
```
</details>


<details>
<summary>클래스와 구조체를 사용하는 이유를 나열하고 객체지향 프로그래밍의 네 가지 특징을 설명합니다.</summary>

```swift
//갭상추다
//캡슐화, 상속화, 추상화, 다형성
```
</details>


<details>
<summary>저장 속성(Stored properties)의 개념을 설명하고 저장 속성을 사용한 예제를 작성합니다.</summary>

```swift
//저장 속성은 클래스나 구조체나 할 것 없이 인스턴스에 소속된 특성이다.
//상수나 변수로 선언가능하다.
class T1 {
  var faker = "god"
}

print(T1.faker)
```
</details>


<details>
<summary>지연 저장 속성(Lazy stored properties)의 개념을 설명하고 관련 예제를 작성합니다.</summary>

```swift
//답변
```
</details>


<details>
<summary>지연 저장 속성을 사용하는 이유에 대해 설명합니다.</summary>

```swift
//처음 접근할 때 초기화가 일어난다(메모리 낭비 방지)
struct IPhone {
    var name: String
    init(name: String) {
        self.name = name
        print("\(name)는 IPhone을 갖고 있습니다")
    }
}

class Person {
    let name: String = "Daniel"
    var age: Int = 30
    lazy var phone = IPhone(name: name)
}
```
</details>


<details>
<summary>Swift에서 메서드의 메모리 구조를 설명합니다.</summary>

```swift
//일반적으로 메서드가 처음 호출되면 해당 메서드의 실행을 위해 스택에 쌓인다.
// 클래스 메서드는 메모리 영역의 frame에서 코드 영역으로 직접 pointed된다.
```
</details>


<details>
<summary>계산 속성(Computed properties)를 정의하고 관련 예제를 작성하여 설명합니다.</summary>

```swift
//속성의 호출 시점 또는 설정 시점에 액션이 일어나도록 프로퍼티 정의에서 get과 set을 설정하는 프로퍼티.

struct Rect {
	...
    
    var center: Point {
        get {
            let centerX = origin.x + (size.width / 2)
            let centerY = origin.y + (size.height / 2)
            return Point(x: centerX, y: centerY)
        }
        set(newCenter) {
            origin.x = newCenter.x - (size.width / 2)
            origin.y = newCenter.y - (size.height / 2)
        }
    }
    
    ...
}

//newValue를 사용하는 것이 좋다
```
</details>


<details>
<summary>계산 속성의 메모리 구조를 설명합니다.</summary>

```swift
//결국 저녀석도 성격은 메서드에 가깝기 때문에 데이터 영역에서 직접 코드로 pointed 되어있다.
```
</details>


<details>
<summary>타입 속성(Type properties)를 정의하고 관련 예제를 작성합니다.</summary>

```swift
//static 영역 즉 데이터 영역에 정의된 타입 frame에 직접 저장되는 프로퍼티
//타입에서 직접 사용 가능
class Human {
    static let name: String = "jinyong"     // 저장 타입 프로퍼티
    static var alias: String {             // 연산 타입 프로퍼티
        return name + "은 뭘로 이루어져 있나"
    }
}
```
</details>


<details>
<summary>계산 타입 속성(Computed type properties)을 설명하고 예제를 작성합니다.</summary>

```swift
//위에 참고
//이녀석도 마찬가지로 타입에서 직접 사용 가능하다. 나머지는 그냥 타입 속성과 별반 차이가 없다.
```
</details>


<details>
<summary>속성 감시자의(Property observers) 개념을 설명하고 클래스 또는 구조체에서 속성 감시자를 사용하는 예제를 작성합니다.</summary>

```swift
//계산 프로퍼티와 비슷하게 set을 이용해서 해당 프로퍼티가 설정되기 전 그리고 설정되기 후의 액션을 지정할 수 있다.

var name: String = "tempt" {
    willSet {
        print(newValue)
    }
    
    didSet {
        print(oldValue)
    }
}
```
</details>





<details>
<summary>추가할 질문이 있다면 해당 양식 복사해서 붙여넣을 것!</summary>

```swift
//답변
```
</details>

