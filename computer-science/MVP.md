# MVP패턴

MVP 패턴은 Model + View + Presenter 가 합쳐진 용어이다.<br/>
Model 과 View는 MVC 패턴과 같고, Controller 대신 Presenter 가 존재한다.<br/>
<br/><br/><br/><br/><br/>

> Presenter

View에서 요청한 정보로 Model을 가공하여 View에 전할해주는 역할을 담당한다.<br/>
View와 Model 사이에 위치하여 데이터 이동을 중계한다.<br/>
Presenter는 View와 Model의 인스턴스를 가지고 있다.<br/>
Presenter와 View는 1:1 관계이다.<br/>
<br/><br/><br/><br/>

> 장점

View와 Model의 의존성이 없다는것이 특징이자 장점이다. MVP 패턴은 Presenter를 통하여 데이터를 전달 받기 때문에 
View와 Model은 서로 독립적이며, Presenter가 기본적으로 Controller와 같은 역할을 하지만, View에 연결되는 것이 아니라
Interface에 연결된다는 점이 다르다.<br/>
이에 따라 MVC가 가진 테스트 가능성 문제와 함께 모듈화/유연성 문제도 역시 해결이 가능해진다.<br/>
<br/>
<br/>

> 단점

View와 Presenter 사이의 의존성이 높다는 단점이 있다. 어플리케이션이 복잡해질 수록 View와 Presenter 사이의 의존성이 강해지는 단점이 있다.

