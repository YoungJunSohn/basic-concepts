# 디버깅을 하는 이유?

얼마 전 "더 나은 개발자로 성장하는 팁" 이라는 영상을 보고 나서<br/>
"아! 디버거를 꼭 사용해야겠구나!"하는 생각이 들었다.<br/>
부끄럽지만, 여지껏 프로젝트를 하면서 디버거를 한번도 사용해본 적이 없었다.<br/>
<br/>
물론 테스트코드도 짜보고, log4j를 통해 로깅을 해보기는 했지만<br/>
IDE에서 제공하는 파워풀한 기능인 디버거를 한번도 사용해 본 적이 없다는 사실에 얼굴이 뜨뜻해졌다.<br/>
<br/>
디버거를 사용하는 이유를 알기 전에, 우선 다음 사례를 보자<br/>
이 사례는 How to be a Programmer 라는 책을 번역한 https://codingnuri.com/learn-to-debug/ 포스팅에서 언급한 내용이다.<br/>
<br/>
<br/>
---

> 사례

대형 소프트웨어 회사에서 구입한 소프트웨어라면 대개 프로그램의 내부를 살펴볼 수 없습니다.<br/>
그럼에도 코드가 문서와 맞지 않는 부분이 있다거나(프로그램이 시스템과 충돌하는 것이 가장 흔하고도 심각한 예입니다.)<br/>
문서화되지 않는 부분이 분명 있을 것입니다. 더 흔히 볼수 있는 경우는 오류가 발생해서 작성한 코드를 조사했는데<br/>
어떤 문제가 발생해서 오류가 생긴 것인지 실마리를 잡을 수 없는 경우입니다.<br/>
이것은 결국 어떤 가정이 올바르지 않거나, 예상치 못한 특정 조건이 발생했음을 의미합니다.<br/>
간혹 소스코드를 뚫어져라 쳐다보면 해결되는 경우도 있습니다만, 그렇지 못한 경우에는 프로그램을 디버깅해야 합니다.<br/><br/>
<br/>

프로그램의 실행 과정에 대한 가시성을 확보하기 위한 방법은 코드를 실행하고, 코드에 관한 사항을 관찰하는 것이다.<br/>
이것은 화면에 표시되는 경우도 있지만, if문처럼 눈에 보이지 않는 조건들이나 복잡한 자료구조가 담겨 있는 경우가 많다.<br/>
이렇게 숨겨진 것들을 드러내야만 한다.<br/>
<br/>
*실행 중인 프로그램의 "내부상황"을 살펴보는 방법은 세 가지가 있다.*<br/>
<br/>
첫 번째, 로깅 : 로그의 형태로 프로그램 실행을 언제나 확인하는 방법<br/>
두 번째, 코드 줄 출력 : System.out.println() 과 같은 형태로 정보를 출력하는 줄을 추가하는 식으로 프로그램을 임시로 수정하는 방법<br/>
세 번째, 디버깅 : IDE의 디버깅 도구를 사용하는 방법<br/>
<br/>
디버깅하는 방법을 찾아보니, 의외로 간단했다.<br/>
짜 놓은 코드에서 라인 번호 부근을 클릭해 breaking point를 만든다.<br/>
-디버거를 실행하면 이 breaking point에서 프로그램 실행을 멈추고 개발자의 다음 명령을 기다리게 된다.<br/>
디버거를 눌러 코드를 실행한다.<br/>
<br/>
<br/>
이렇게 하면 디버거가 실행되며 코드가 처음부터 끝까지 읽히지 않고 breaking point까지만 실행된다.
여기서부터 코드를 한줄 한줄 확인할 수 있는 것이다.<br/>
<br/>
앞으로 코딩을 할 때는 반드시 디버거를 사용해 볼 생각이다.<br/>