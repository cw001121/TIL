# ✨ JAVASCRIPT OVERVIEW ✨

## **Javascript**

- 객체 기반의 스크립트 언어
  - 웹 문서에서 사용자와 다양한 상호작용을 하기 위해 만들어짐
  - 각각의 웹 브라우저용 전용 스크립트 존재 &rarr; 현재 Javascript로 표준화
  - 현재는 웹 브라우저에서만 사용되지 않고 Node.js를 통해 다양한 프로그램에 응용된다
- HTML (웹 페이지 생성) &rarr; Javascript (사용자와의 상호작용 추가)
  - HTML은 정적, Javascript은 동적이다

## **HTML와 접목**

- script 태그
  - 태그 안 javascript 코드를 집어넣음

```html
<script>
  ...
</script>
```

- 이벤트
  - 웹브라우저 위에서 발생되는 이벤트를 javascript 코드로 처리
  - 마우스 이벤트, 키 이벤트, 폼 이벤트, 로드 및 기타 이벤트 존재

```html
<input type="button" onclick="alert('hi')" />
```

- 콘솔 : 콘솔창에서 편집하여 바로 실행 가능

## **CSS를 동적으로 사용**

```javascript
document.querySelector("선택할 태그").속성.속성 = "값";
document.querySelector("선택할 태그").style.backgroundColor = "black";
```

## **async**

1. <head>안 script를 추가할 경우, 브라우저가 한줄한줄 분석함 -> CSS와 병합해서 DOM?요소로 변환함 -> 처음부터 다운로드, 실행 기다렸다가 html 시작

- 웹 브라우저가 html 페이지를 인식하는 방식을 의미 / 문서 객체와 관련된 객체의 집합 또한 의미
- 단점 : js 파일이 클 경우, 느려짐

2. <body> 끝부분에 추가할 경우, script를 다운로드 받고 있는다고 해도 이미 사용자가 컨텐츠를 보고 있을 수 있음! - html을 하다가 중간에 다운로드 받고 실행하는 거 기다렸다가 html 재시작

- 단점 : 웹사이트가 자바스크립트에 의존적이라면 사용자가 정상적인 페이지를 보기 전까지는 기다려야함

3. head + async :async은 불리언 타입의 속성값이므로 선언하는 것만으로도 true로 선언이 되어 다운로드를 먼저 하되 실행할 때는 멈추고 다시 실행하고 html 재시작
<script async src = ".js">

- 다운로드 시간 절약
- 조작 시점에 html이 아직 정의되지 않았을 수 있음

4. head + defer : 가장 좋은 옵션
<script defer src = ".js">
먼저 다운로드를 받아놓은 다음에 사용자에게 tml 화면을 출력해주고 자바스크립트를 실행

- async vs defer
  - async의 경우, 순서에 상관없이 다운로드 먼저 된 것부터 실행 (실행하는 동안 html 멈춤) : 순서에 의존적이면 문제가 됨
  - defer : 먼저 다 다운로드를 받아놓은 후 (parsing HTML 동안) 다 됐을 경우, 실행은 순차적으로 한다

'use strict' --> 상식적인 범위 안에서 자바스크립트를 사용할 수 있게 해줌
--> 선언하기 전 사용하는 등을 막아줌