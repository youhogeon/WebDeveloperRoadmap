# HTML
본 문서에서는 기본적인 문서를 작성하기 위해 배워야할 내용들을 HTML 태그 위주로 다룹니다. HTML의 간단한 역사가 포함되어 있으며, HTML5에서 새로 생긴 태그들 또한 포함되어 있습니다.

HTML 파일은 텍스트 에디터(VS Code, Editplus 등)를 사용하여 html 확장자로 저장한 후 웹서버를 이용해 구동하는 것이 일반적이나, [JSFiddle](https://jsfiddle.net) 등과 같은 온라인 코드 작성 도구를 이용해 연습할 수도 있습니다.

## 차례
1. [정의](#정의)
1. [HTML의 역사](#html의-역사)
1. [태그의 구조](#태그의-구조)
1. [HTML 기본 구조](#html-기본-구조)
1. [`<head>`에 담기는 태그](#head에-담기는-태그)
1. [기본 태그](#기본-태그)
1. [고급 태그](#고급-태그)
1. [참고 자료 및 출처](#참고-자료-및-출처)

## 정의
HTML은 하이퍼텍스트 마크업 언어(HyperText Markup Language)의 약자로, **웹 페이지를 위한 마크업 언어**다. HTML은 제목, 단락, 목록 등과 같은 본문을 위한 구조적 의미를 나타내는 것뿐만 아니라 링크, 인용과 그 밖의 항목으로 구조적 문서를 만들 수 있는 방법을 제공한다. [(출처 : Wikipedia)](https://ko.wikipedia.org/wiki/HTML)

**웹 페이지의 기본적인 틀**을 만들때에는 HTML이 사용된다. 이 HTML에 CSS를 이용하여 스타일을 더하고, Javascript를 이용하여 액션(이벤트 등)을 더하면 프론트앤드 웹이 만들어진다.

## HTML의 역사
HTML의 초안은 1980년 공개되었으나, 일반적으로 대중에 공개된 것은 1991년이다. 당시에는 20개의 태그를 이용하여 문서를 작성하였으며(이 중 13개는 HTML4에도 여전히 존재한다.) 1995년 HTML 2.0, 1997년 초 HTML 3.2을 거쳐 1997년 말 HTML 4.0이 공개된다.

HTML 4.0은 HTML 5.0 (이하 HTML5)이 공개되기 전까지, XHTML과 함께 10년 넘게 웹을 지배해왔다.

그리고 마침내 2008년, HTML5가 공개되었고, HTML5의 공개와 브라우저 시장의 발전으로(기존에는 브라우저별로 각기 다른 표준을 가지고 있었고, 개발된 프론트앤드가 브라우저별로 각각 다르게 표현되는 경우가 많았다.) 프론트앤드 웹은 빠르게 발전해왔다.

## 태그의 구조
HTML 문서는 기본적으로 **태그**라는 요소로 이루어져 있다.
태그의 구조는 아래와 같다.

`<태그명 속성명="속성값" 속성명2="속성값2">태그 본문</태그명>`
태그는 여는 태그(`<태그명>`)과 태그 본문, 닫는 태그(`</태그명`) 으로 이루어져 있으며, 여는 태그에는 태그의 속성을 명시할 수 있다.

예를 들어, 하이퍼링크를 만드는 a 태그의 경우, 하이퍼링크의 주소를 의미하는 href 속성을 가지는데, 이 경우 아래와 같이 태그를 작성할 수 있다. [[결과물 보기 - JSFiddle]](http://jsfiddle.net/ge0ucdsp/)

`<a href="http://www.google.com">Go to Google</a>`


## HTML 기본 구조
HTML5의 기본 구조는 아래와 같다.

```
<!-- File : index.html -->
<!doctype html>
<html>
  <head>
    <title>Hello HTML</title>
  </head>
  <body>
    <p>Hello World!</p>
  </body>
</html>
```
첫 번째 줄에는 문서 형식 선언(document type declaration, `<!doctype html>`)이 담긴다.

HTML4의 문서 형식 선언이 `<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">` 인 것과 비교해 볼 때, HTML5의 문서 형식 선언은 상당히 간결해진 모습을 볼 수 있다.

문서 형식 선언 아래에는 `<html>` 문서의 본문이 담기는 태그가 있고, `<html>`태그 속에는 문서의 정보가 담기는 `<head>` 태그와, 브라우저에 랜더링되는 내용(본문)이 담기는 `<body>` 태그가 있다.

이 때, 한 태그를 감싸고있는 태그를 **부모 태그(parent tag)** 라고 부르며, 한 태그 속에 담긴 태그들을 **자식 태그(child tag)** 라고 부른다. 예를 들어, 위 문서에서 `<head>`는 `<title>`의 부모이고, `<p>`는 `<body>`의 자식이다.

## head에 담기는 태그
`<head>` 태그에 담기는 태그 중 대표적인 태그는 아래와 같다.

* `<title>` : 문서의 제목을 표현한다.
* `<meta>` : 문서의 정보를 표현한다. 일반적인 웹 사용자에게는 보이지 않으며, 주로 검색 엔진이나 브라우저 등에 현재 문서에 대한 정보를 제공하기 위해 사용한다.
* `<link>` : 외부 CSS 파일을 불러오기 위해 사용한다.
* `<style>` : CSS를 문서 내에 작성하는 경우 사용한다.
* `<script>` : Javascript를 문서 내에 작성하거나, 외부 Javascript 파일을 불러오기 위해 사용한다. (Javascript가 아닌 VBScript(IE)나 Coffeescript 등 다른 script를 불러오기도 한다.) `<script>` 태그는 `<body>` 내에서도 사용할 수 있다.

## 기본 태그
`<body>` 태그에 담기는 태그 중 필수적으로 알아야 할 태그는 아래와 같다.  HTML5 명세에서 새로 생긴 태그도 포함하였다.

* `<!-- Comment -->` : 브라우저가 랜더링하지 않는 주석을 나타낸다. 주로 코드에 설명을 달기 위해 사용한다.
* `<h1>` ~ `<h6>` : 제목을 표현하기 위해 사용한다. `<h1>`은 최 상단 제목을 나타내며, `<h2>`에서 `<h6>`으로 갈 수록 더 작은 소제목을 의미한다.
* `<br>` : 줄바꿈을 나타낸다.
* `<hr>` : 구분선을 나타낸다.
* `<b>`, `<i>`, `<u>`, `<s>` : 각각 두꺼운 글씨, 기울어진 글씨, 밑줄 글씨, 취소선 글씨를 나타낸다.(HTML4) HTML5에서는 태그의 의미가 다소 변경되었다. 예를 들어, 단순 강조를 위해서는 `<b>` 태그가 아니라 `<em>` 태그를 사용하도록 변경되었으며, 작품의 제목을 표시하기 위해서는 `<i>` 태그가 아니라 `<cite>` 태그를 사용하도록 변경되었다. 이는 검색엔진 등이 태그만 보고도 태그 속 내용을 유추할 수 있도록 하기 위함이다.
* `<p>` : 문단을 정의한다. 브라우저상에는 약간의 여백을 제외하고는 나타나지 않으며, 문단별로 다른 스타일이나 스크립트를 적용하기 위해 사용하기도 한다.
* `<div>` : 문서에서 태그들을 묶는 컨테이너로 사용된다. HTML5에서는 `<div>`태그가 좀 더 세분화 되어, 링크들을 묶는 컨테이너인 `<nav>`, 헤더(로고, 사이트명 등)를 묶는 컨테이너인 `<header>` 등의 시멘틱 태그가 추가되었다. (여전히 `<div>`도 유효하며 자주 사용된다.)
* `<span>` : `<div>`과 같은 목적으로 사용되나, `<div>`의 경우 컨테이너간 줄바꿈이 이루어지며(CSS의 block 요소), `<span>`의 경우 줄바꿈이 이루어지지 않는다. [[예제 - JSFiddle]](http://jsfiddle.net/1gaq8nw4/)
* `<form>` : 다른 페이지로 정보를 보내기 위한 폼을 정의하는데 사용한다. `<form>` 태그 안에는 `<input>`이나 `<textarea>` 등 폼 요소 태그가 들어간다. (폼 요소라고 해서 반드시 `<form>` 내에서 사용할 필요는 없다.)
* `<input>` : type속성을 이용해 텍스트박스, 체크박스, 라디오, 버튼 등을 만드는데 사용한다. HTML5에서는 type속성이 더 추가되어, 이메일을 입력받거나, 달력을 띄우는 것도 가능하며, 작성된 요소를 검증하는 required 속성 등 많은 속성이 추가되었다.
* `<textarea>` : 여러 줄을 입력할 수 있는 글상자를 만든다.
* `<button>` : 버튼을 만든다. 반드시 `<form>` 내에서 사용할 필요는 없으며, `<form>`과 직접적인 연관이 없다. `<form>`내에서 사용하는 전송 버튼을 만들 때는 보통 `<input>` 태그를 사용한다. (`<input type="submit" value="전송">`)
* `<select>`, `<option>` : 선택 상자(콤보박스)를 만든다.
* `<label>` : 각각의 폼 요소에 설명을 추가한다. label 요소를 마우스로 클릭하는 경우 해당 폼 요소에 포커스가 이동한다. [[예제 - JSFiddle]](http://jsfiddle.net/wypjvsog/)
* `<a>` : 하이퍼링크를 만든다.
* `<iframe>` : 다른 문서를 문서 내에 포함하는 문서를 만든다. HTML5에서는 `<ifrmae>`을 제외한 프레임 태그(`<frameset>` 등)가 모두 제거되었다.
* `<img>` : 이미지를 추가한다.
* `<ul>`, `<ol>` : 각각 순서가 없는 리스트, 순서가 있는 리스트를 만든다. 리스트의 항목은 `<li>` 태그를 자식으로 이용하여 생성한다. `<ul><li>list 1</li><li>list 2</li></ul>`
* `<table>`, `<tr>`, `<td>` : `<table>`태그는 표를 만드는데 사용하며, `<tr>`과 `<td>`를 이용하여 행과 열을 작성한다.

## 고급 태그
본 섹션에 담긴 태그 중 `<noscript>`를 제외하고는 모두 HTML5에서 새로 추가된 태그이다. HTML5에서는 그만큼 더 나은 웹을 만들기 위한 고급스러운 태그가 많이 추가되었다.
* `<canvas>` : 자바스크립트를 이용하여 그림을 그릴 수 있는 영역을 추가한다. `<canvas>` 태그로 인하여 일부 이미지의 경우 `<img>` 태그 없이 표현하는것이 가능해졌으며, 웹 게임을 만드는 것도 가능해졌다. [[Canvas 예제 - JSFiddle]](http://jsfiddle.net/9mwxqs36/), [`<canvas>`로 만든 pacman 게임](https://www.crazygames.com/game/pacman-io)
* `<audio>`, `<source>` : 문서에 소리 재생기를 추가한다. HTML5 이전에는 플래시 등 외부 기술을 이용하여 문서에 소리를 추가하였으나, HTML5부터는 표준 기술로 자리잡았다.
* `<video>`, `<source>` : 문서에 영상 재생기를 추가한다. `<audio>`와 마찬가지로 HTML5부터 표준으로 추가되었다.
* `<noscript>` : 브라우저에서 자바스크립트를 사용할 수 없는 경우(시각장애인용 브라우저 등) 표시할 텍스트를 감싼다.

아래는 시멘틱 태그이다. 시멘틱 태그는 HTML5에서 도입된 개념으로, 검색 엔진 등이 해당 태그 안의 내용을 유추할 수 있도록 도와준다. 시멘틱 태그는 문서에 하나만 존재할 필요는 없으며, 중복 사용을 허용한다.
* `<nav>` : 링크들을 담는 시멘틱 태그이다. `<div>`과 마찬가지로 문서상에는 표현되지 않는다.
* `<header>` : 헤더 요소(로고 등)를 담는 시멘틱 태그이다.
* `<section>` : 섹션을 표현하는 시멘틱 태그이다.
* `<article>` : 본문을 표현하는 시멘틱 태그이다.
* `<footer>` : 푸터 요소(Copyright 등)을 담는 시멘틱 태그이다.

## 참고 자료 및 출처
* [HTML5 Reference - HTML 태그 모음](https://www.w3schools.com/tags/ref_byfunc.asp)
* [HTML Wikipedia](https://en.wikipedia.org/wiki/Html)
* [JSFiddle](https://jsfiddle.net)
