# ✨ HTML OVERVIEW ✨

## **웹이란?**

### **웹**

- 월드 와이드 웹(World Wirde Web) : 인터넷 망으로 연결된 사용자 또는 컴퓨터들이 정보를 공유할 수 있는 네트워크

### **특징**

- 하이퍼미디어

|                   멀티미디어                   |                            하이퍼텍스트                             |                    하이퍼미디어                     |
| :--------------------------------------------: | :-----------------------------------------------------------------: | :-------------------------------------------------: |
| 시각적, 청각적 매개체를 디지털로 통합하여 전달 | 문서와 문서 사이 연결 <br>&rarr; 문자를 클릭하여 연결된 문서로 이동 | 문자뿐만 아닌 다른 매체 또한 연결해놓은 미디어 형식 |

&rarr; 해당 연결된 관계를 인터넷 망으로 연결한 것!

### **구성**

- 프런트엔드 : UI/UX를 개발하는사용자에게 보여지는 외관 개발
- 백엔드 : 어떤 데이터가 보여질지 정리하고 가공하는 로직 개발
- 데이터베이스 : 데이터를 저장하고 꺼낼 수 있는 공간을 구성, 관리

웹 브라우저 (클라이언트) &rlarr; 웹 서버 <br>
&rarr; 응답이 우리의 화면에 전달됨

## **HTML이란?**

### **HTML**

- HTML (HyperText Markup Langauge) : 웹을 이루는 가장 기초적인 구성 요소로, 웹 페이지의 내용을 서술하고 정의하는 데 사용
  - 렌더링 엔진 : HTML과 CSS 등을 읽어와 사람이 읽을 수 있는 문서로 표시하는 소프트웨어
  - 해당 브라우저의 엔진으로 HTML을 읽어 표시하는 것!

### **특징**

- 하이퍼텍스트를 가장 중요한 특징으로 하는 _마크업 형식_ 컴퓨터 프로그래밍 언어
  - 태그라는 개념으로 구분 &rarr; 웹 화면의 요소(element)를 표현
  - 소단위인 태그 집합으로 하나의 큰 정보를 표현
- DOM (문서 객체 모델)
  - 문서 내의 모든 요소, 각각의 요소에 접근하는 방법을 구조화하여 표현

## **문법**

- 여는 태그와 닫는 태그의 하나의 쌍
- 태그는 중첩될 수 있다 &rarr; 웹 컨텐츠와 구조를 결정한다

### **태그 구조**

- 여는 태그 (태그네임, 태그타입) / 내용 (컨텐츠) / 닫는 태그 으로 구성

### **속성**

- 속성은 순서 상관 X
- 속성 이름에 따라 기능이 존재 &rarr; 형식에 따라 달아주면 됨

## **HTML의 기본 구조**

### **html 표준 명시**

- 가장 상위 태그

```html
<!Docutype html>
```

### **meta 태그**

- 페이지가 어떠한 정보를 가지는지 설명하는 태그 = meta data
- 실제 화면에 나오진 않지만 해당 페이지를 설명하는 것!

```html
<meta charset="utf-8" />
: 글씨 타입을 utf-8로 지정
<meta name="description" content="설명 내용" /> : name으로 설명할 부분을 지정한
후, content로 설명 내용 작성 <meta http-equiv="refresh" content="30" /> : 30초
간격으로 리프래쉬하는 것
```

### **block vs inline**

- block : 공간이 남아도 다음 줄로 넘어감
- inline : 공간이 남으면 옆에 배치 &rarr; 한 줄에 꽉 채워야 넘어감

### **의미론적인(semantic) 태그**

- 의미를 부여하여 사이트의 구조를 쉽게 파악하고자 하는 태그
- 기존에는 `<div id="header">`과 같이 사용하였음
- 어떠한 기능 및 변화가 없지만 의미를 파악하도록 함

- header / nav / section / article / aside / footer 구성
  |header| nav |body |aside| main| footer|
  |:--:|:--:|:--:|:--:|:--:|:--:|
  |문서의 가장 윗 부분|목적지로 이동할 수 있도록 링크를 별도로 모아놓은 영역|특정 구역을 나타냄|자체로 독립적인 내용 표현|사이드바 영역|문서 맨 아래쪽|
  |사이트 로고, 헤드라인, 검색창 등||소개, 본문, 연락처 등|뉴스기사, 포스트 등|배너, 용어 설명, 관련 상품 등|저작권, 연락처 등|

```html
<header></header>
<footer></footer>
<article></article>
<section></section>
```

### **주석**

```
<!-- 주식 내용 ... -->
```

### **html, head, body 태그**

|         html          |                      head                       |               body               |
| :-------------------: | :---------------------------------------------: | :------------------------------: |
| 문서의 시작과 끝 정의 | 메타 정보를 정의, 사용자가 볼 수 없는 영역 담당 | 실제 사용자에게 보여질 화면 구현 |

### **title**

- 탭의 제목 변경

```Html
<title></title>
```
