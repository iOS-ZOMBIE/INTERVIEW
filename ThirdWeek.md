# [iOS 🧟 ZOMBIE] iOS 인터뷰 - 3주차

스스로 설명할 수 있을 만큼의 인터뷰 능력을 기르는데 중점을 뒀습니다.

앨런29기 진도에 맞춰, 각 주차별로 준비한 인터뷰 문제를 풀어보고, 질문합니다.

<br>

<details>
<summary>스위프트에서 클래스와 구조체의 차이점을 설명합니다.</summary>

```swift
// 클래스는 reference type이며 인스턴스가 메모리 영역에서 heap에 저장됩니다. 구조체는 value type으로 인스턴스가 stack 영역에 저장됩니다. reference type은 값의 복사가 일어날때 실제적으로는 인스턴스를 가리키는 메모리 주소의 복사가 일어나기 때문에 원본값과 복사된 값이 같은 메모리 영역을 가리키기 때문에 한쪽에서 수정이 일어나면 다른쪽에도 반영됩니다. 반면에 value type은 인스턴스의 복사가 일어날때 인스턴스 자체가 복사가 일어나기 때문에 한쪽에서 수정이 일어나도 다른쪽에는 영향이 없습니다. 또한 메모리 영역 특성상 stack에서의 읽기/쓰기가 heap 영역의 읽기/쓰기보다 빠르기 때문에 보편적으로는 구조체가 클래스보다 빠릅니다. 애플에서도 구조체를 사용할 수 없을때 클래스를 사용하라고 해놨습니다. 또 구조체는 상속이 되지 않지만 클래스는 상속이 가능합니다.  
```
</details>


<details>
<summary>클래스(참조 유형)와 구조체(값 유형) 간의 메모리 관리 차이를 설명합니다.(인스턴스의 복사와 관련하여 설명할것)</summary>

```swift
// 클래스(referece type)의 인스턴스는 heap영역에 생성되고 해당 인스턴스를 가리키는 메모리 주소를 stack 영역의 변수에 할당합니다. 값의 복사가 일어날때 해당 메모리 주소를 복사해서 변수에 할당합니다. 따라서 한쪽에서 수정이 일어나면 다른쪽에도 수정된 사항이 반영이 되는걸로 보여집니다. 반면에 구조체(value type)은 인스턴스 생성을 stack 영역에서 해서 변수에 할당합니다. 인스턴스의 복사가 일어날때 해당 인스턴스 자체를 복사해서 다른 변수에 할당합니다. 그렇기 때문에 한쪽에서 값의 변화가 일어나도 다른쪽에 영향을 끼치지 않습니다. 
```
</details>


<details>
<summary>구조체의 상수 인스턴스를 선언하는 방법을 보여주고 속성이 변경되었을 때 그 동작을 설명합니다.</summary>

```swift
// 
```
</details>


<details>
<summary>스위프트에서 초기화의 의미에 대해 설명합니다.</summary>

```swift
// 초기화란 특정 타입의 인스턴스를 생성하는 과정을 의미합니다. 타입에 따라 초기화 과정에서 초기화 함수에 파라미터를 넣어줘야하는 등 초기화함수가 요구하는 것들을 해야할 수 있습니다. 또한 커스텀 초기화 함수를 이용해서 특정 타입의 초기화 과정을 커스텀할 수 있습니다.
```
</details>


<details>
<summary>클래스와 구조체의 초기화 과정을 비교해서 설명합니다.</summary>

```swift
// 클래스는 초기화 과정에 인스턴스가 heap 영역에 생성됩니다. 그리고 해당 인스턴스를 카리키는(인스턴스의 메모리주소를 갖고 있는) 변수가 stack영역에 저장이 됩니다. 반면에 구조체의 인스턴스는 stack 영역에 생겨서 변수에 직접 저장이 됩니다. 
```
</details>


<details>
<summary>클래스와 구조체를 사용하는 이유를 나열하고 객체지향 프로그래밍의 네 가지 특징을 설명합니다.</summary>

```swift
// 클래스와 구조체를 사용하는 이유는 데이터를 우리가 원하는 데이터를 묶어서 사용할려고 하기 때문입니다. 현실세계의 특정 물체에 대해서 우리가 필요한 정보를 모아서 클래스 혹은 구조체로 모델링하는것이 객체지향 프로그래밍의 특징 중 하나인 추상화라고 합니다. 이 모델링된 형태를 실제 코드로 구현하여 하나의 객체로 묶어내는 과정을 객체지향 프로그래밍의 특징 중 하나인 캡슐화라고 합니다. 캡슐화 과정에서 접근제어자를 잘 설정해서 외부에서 객체의 정보에 함부로 접근하지 못하게 하는것을 은닉화라고 합니다. 이 캡슐화된 객체를 필요에 따라 하위 클래스로 속성과 메서드를 내려서 사용할 수 있게 하는것이 객체지향 프로그래밍의 특징인 상속이라고 합니다. 마지막으로 상속받은 하위 객체에서 필요에 따라 재정의해서 사용하는것을 객체지향의 특징인 다형성이라고 합니다. 
```
</details>


<details>
<summary>저장 속성(Stored properties)의 개념을 설명하고 저장 속성을 사용한 예제를 작성합니다.</summary>

```swift
// 저장속성이란 해당 인스턴스에서 메모리에 저장해서 사용해서 사용하는 속성을 뜻합니다. 
class StoredPropertyClass {
    var number: Int
    
    init(number: Int) {
        self.number = number
    }
}
```
</details>


<details>
<summary>지연 저장 속성(Lazy stored properties)의 개념을 설명하고 관련 예제를 작성합니다.</summary>

```swift
// 지연 저장 속성은 저장 속성이지만 인스턴스를 생성할때 메모리에 올라가지 않는 속성입니다. 추후에 지연 저장 속성에 접근(읽기 혹은 쓰기)를 할 때 메모리에 올라가기 때문에 메모리의 부담을 줄여주는 속성입니다. 
class LazyStoredPropertyClass {
    lazy var lazyNumber: Int = 1
}
```
</details>


<details>
<summary>지연 저장 속성을 사용하는 이유에 대해 설명합니다.</summary>

```swift
// 메모리에 부담을 줄여주기 위해서 입니다. 간단한 저장 속성의 경우에는 큰 문제가 되지 않지만 이미지처럼 사이즈가 큰 값들을 인스턴스의 생성과 함께 메모리에 올린다면 초기화 과정에서 부담이 되고 또한 사용하지 않는다면 해당 크기만큼의 메모리가 낭비됩니다. 이럴때 지연 저장 속성을 이용한다면 꼭 필요할때 해당 값이 메모리에 올라가기 때문에 메모리 낭비를 줄일 수 있습니다.
```
</details>


<details>
<summary>Swift에서 메서드의 메모리 구조를 설명합니다.</summary>

```swift
// Swift에서 메서드는 코드의 묶음입니다. 메서드의 코드는 컴파일되어서 코드 영역에 저장되고, 타입의 메서드는 해당 코드 영역의 시작 지점을 카리키게 됩니다. 따라서 메서드를 실행시키면 해당 타입으로 간 다음에 해당 타입에 메서드를 저장해놓은 배열에서 메서드를 찾아서 해당 메서드가 있는 코드 영역으로 이동해서 코드를 실행시킵니다.
```
</details>


<details>
<summary>계산 속성(Computed properties)를 정의하고 관련 예제를 작성하여 설명합니다.</summary>

```swift
// 계산 속성은 실질적으로는 메서드입니다. 계산 속성의 getter와 setter는 실질적으로는 메서드로 구현되어 있으며, 읽기/쓰기를 코드에서 할려고 할때마다 이 getter 메서드와 setter 메서드가 실행되는것입니다.
struct ComputedPropertyStruct {
    var storedProperty: Int = 1
    var computedProperty: Int {
        get {
            return storedProperty
        }
        set {
            self.storedProperty = newValue
        }
    }
}
```
</details>


<details>
<summary>계산 속성의 메모리 구조를 설명합니다.</summary>

```swift
// 계산 속성의 메모리 구조는 메서드와 유사합니다. 계산속성의 읽기 혹은 쓰기를 요청하면 해당 작업을 하는 코드 영역에 저장된 코드로 메모리 주소를 이동시킵니다.
```
</details>


<details>
<summary>타입 속성(Type properties)를 정의하고 관련 예제를 작성합니다.</summary>

```swift
// 타입 속성은 인스턴스에 부여되는게 아닌 타입에 부여되는 속성입니다. 타입 속성은 보통은 해당 타입과 하위 클래스들에서 필요한 값, 혹은 해당 타입의 인스턴스들이 공통으로 가져야하는 값들을 타입 속성으로 정의합니다.
struct TypePropertyStruct {
    static var typeProperty: String = "Type Property"
}
```
</details>


<details>
<summary>계산 타입 속성(Computed type properties)을 설명하고 예제를 작성합니다.</summary>

```swift
// 계산 타입 속성은 말 그대로 계산 속성과 타입 속성이 합쳐진것입니다. 타입 속성과 마찬가지로 타입에 부여된 속성이지만, 계산 속성과 마찬가지로 메서드의 형태로 존재하는 속성입니다.
```
</details>


<details>
<summary>속성 감시자의(Property observers) 개념을 설명하고 클래스 또는 구조체에서 속성 감시자를 사용하는 예제를 작성합니다.</summary>

```swift
// 속성 감시자는 특정 속성의 변화를 감지하는 역할을 합니다. 속성 감시자를 사용하는 이유는 속성이 변화하는 시점에 특정 동작을 할 수 있게 하기 때문에 유용하게 사용할 수 있습니다.
struct PropertyObserverStruct {
    var propertyObserver: Int = 0 {
        willSet {
            print("값이 변화하기 전")
            print(propertyObserver)
        }
        didSet {
            print("값이 변화한 후")
            print(propertyObserver)
        }
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

