# CSS Triggers

[https://www.lmame-geek.com/css-triggers/](https://www.lmame-geek.com/css-triggers/)

<br>

## 왜 점검해 봐야 하는가?

critical rendering path ⭐

: 브라우저가 하나의 화면을 그려내는 과정 또는 순서

<br>

1. requests/response (html파일 요청)
2. loading
3. scripting (dom요소로 변환)
4. rendering
5. layout
6. painting

<br>

여기서 render를 기준으로

1,2,3 > construction (브라우저만의 언어로 바꾸는)파트 :

DOM, CSSOM, RenderTree

4,5,6 > operation (구조 작성,배치, 그림을 그리는)파트:

layout, paint, composition

<br>

## 여기서 성능을 향상시키려면?

HTML > RenderTree : DOM, CSS가 작을수록 속도가 빨라짐

불필요한 요소 없이 작게 만드는 게 중요.

Operation: 사용자가 클릭을 해서 요소를 움직이거나 애니메이션을 쓸 때

paint가 자주 일어나지 않도록 만드는게 중요.

translate를 이용해서 옮기게 되면 paint는 일어나지 않고 composition만 일어나면 된다. (불필요한 일들이 일어나지 않아서 성능이 괜찮게 동작)

position이 바뀌면 layout부터 다시 변경이 되어야 함. 성능이 나빠질 수 밖에 없다.

<br>

### 결론: js나 css로 dom 요소를 조작할 때 composition만 일어나게 하는게 BEST.

<br><br>

각 브라우저

- blink: 크롬 브라우저

- gecko: 파이어폭스

- webkit: 사파리

- edgeHTML: 구 엣지

<br><br>

결론: opacity, transform > 너무 좋음

top, left를 지양하고 translate 를 지향하자

<br><br>

성능 개선 증거는 f12 > perfomance 에서 측정해볼 수 있다.

frames 얼마 동안에 어떤 프레임이 발생했는지 알 수 있음

summary: 얼마나 시간이 걸렸는지

experience:
사용자가 원만한 경험을 하려면 한 프레임이 보여질 때 **16.67ms** 동안 끝나야 한다.

<br><br><br><br><br>

reference

- https://developer.mozilla.org/en-US/docs/Web/Performance/Critical_rendering_path
- https://velog.io/@mu1616/Critical-Rendering-Path
