#MVVM 패턴

MVVM은 Model + View 와 ViewModel 을 합쳐놓은 디자인 패턴이다.<br/>
MVVM을 구성하는 3가지 요소의 역할과 책임을 이해하기 위해서는 먼저 이들 사이 관계를 알아야 한다.<br/>
<br/>
View는 ViewModel을 알지만 ViewModel은 View를 알지 못한다.<br/>
ViewModel은 Model을 알지만 Model은 ViewModel을 알지 못한다.<br/>
<br/>
이것은 무슨 뜻인가 하면<br/>
ViewModel은 Model로부터 데이터를 가져오는데, 그 데이터는 View에 적합한 데이터로 가공된다. <br/>
이 ViewModel에 포함된 가공된 데이터는 View와 연관되어 있기 때문에 즉각적으로 View에 반영된다.*(핵심)* <br/>
하나의 View에는 하나의 ViewModel이 1:1로 대응되며 View가 여러개일때는 마찬가지로 여러개의 ViewModel이 구성된다.<br/>
<br/>
<br/>
MVVM 패턴은 MVP 패턴과 마찬가지로 View로부터 입력을 받게 된다.<br/>
Model은 View로 직접적으로 응답을 하지 못하고, View 모델로 응답을 하게 된다.<br/>
<br/><br/><br/>
<br/>

> ViewModel의 역할

View Model의 역할은 View가 사용할 메서드와 필드를 구현하고, View에게 상태 변화를 즉각적으로 알리는 것이다.<br/>
View는 ViewModel의 상태 변화를 옵저빙하고 있으며, ViewModel에서 제공하는 메서드와 필드가 UI에서 제공할 기능을 정의한다.<br/>
그러나, View에서 이 기능을 어떻게 보여줄 지를 결정한다.<br/>
<br/>
위에서 설명했듯, View 와 ViewModel은 1:1 대응이지만, ViewModel과 Model은 1:多 관계를 형성한다.<br/>
이것은 또 무슨 뜻인가 하면<br/>
ViewModel은 여러 개의 Model로부터 제공받은 데이터를 가공해서 View에 제공하게 되는데 예를들어 어떤 View에서 서로다른 두 모델의 데이터를 활용한 데이터가 필요하게 된다면 
View에서 이 데이터들을 조작해서 사용하는 것이 아니라, ViewModel에서 가공해서 전달하고, View에서는 오직 UI만 다루도록 해야한다.<br/>
<br/>
<br/>
<br/>


>MVVM 모델의 장점

* Command 와 DataBinding을 통해 MVP패턴과는 달리 View와 Model 간의 의존성을 완벽하게 분리할 수 있다.<br/>
* Command 를 통하여 View의 특정한 이벤트로 input을 받을 수 있으며, ViewModel의 속성과 View의 속성을 Binding 시켜줌으로서 ViewModel 속성이 변경될 때마다 실시간으로 View를 업데이트 시킬 수 있다.<br/>