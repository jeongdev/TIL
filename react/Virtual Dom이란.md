# Vrtual Dom이란?

브라우저가 페이지의 초기 출력을 위해 실행해야 하는 순서 (CRP):

 <br>

1. DOM

2. CSSOM

3. RenderTree (Attachment)

4. Layout

5. Paint

6. Composition

<br> <br>

그 후 JS나 CSS를 통해 DOM 또는 CSS에 변화가 생길 경우,

reflow 혹은 repaint의 과정을 수행하며,

이는 DOM 조작이 많이 일어나는 복잡한 SPA(싱글 페이지 애플리케이션)에는 비효율적이다.

  <br>

그래서 나온 것이 **Virtual DOM(가상돔)** 이다!

  <br>

뷰에 변화가 있다면, 실제 DOM이 아닌 가상 DOM에 먼저 적용시키고, 변화된 부분만 실제 DOM으로 전달함으로써 한 번만 렌더링을 진행한다.

결과적으로 브라우저 내에 연산의 양을 줄이면서 성능 개선이 되는 것이다.

<br> <br>

단점

가상 돔은 메모리에 존재하기 때문에, 메모리의 사용이 늘어난다.
마찬가지로 최적화 작업을 해야한다.
