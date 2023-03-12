# Browser

## **A P I s**:

**A**pplication **P**rogramming **I**nterfaces

<br>
UserStorage = login, logout

브라우저마다 공통으로 제공하기로 약속한 api

(이런게 가능하구나 정도로 알아두자)

1. DOM APIs
2. Network APIs
3. Graphics APIs
4. Audio/Video APIs
5. Device APIs
6. File APIs
7. Storage APIs

MDN Web API: [https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Client-side_web_APIs/Introduction](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Client-side_web_APIs/Introduction)

<br>

## **HTTP**: Hypertext Transfer Protocal

클라이언트가 서버에 정보를 요청하고, 다시 받아오는 방식으로 이루어져 있다.

## **HTTPS**: Hypertext Transfer Protocal Secure

http에서 서버에 비번을 입력하면 비번이 그대로 전송되서, 해커가 들여다볼 수 있음

https는 비번이 암호키로 보안처리가 되어서 전송되서 들여다볼 수 없음

<br>

window의 구성

- DOM - document

- BOM - navigator, location, fetch, storage…

- Javascript - Array, Map, Date

기본적으로 WINDOW는 글로벌 object 기 때문에

아무런 object를 지정하지 않았다면 window를 가르킴.

<br>

## **DOM**: **D**ocument **O**bject **M**odel

html tag > javascript node 변환

node > 모든 node는 event 가 발생할 수 있다. node는 event target을 상속한다

<br>

cssom : css object model

DOM + css (external, embedded, inline, user-agent stylesheet) = CSSOM (compute styles, based on css, cascading rules)

부모에 css 설정을 하면 cascading rules에 따라서 밑에 애들도 적용됨

DOM + CSSOM = Render Tree

render tree에는 사용자에게 궁극적으로 보여지는 애들만 선별이 된다

span opacity: 0 / visibility: hidden 은 포함 되지만 display none는 x
