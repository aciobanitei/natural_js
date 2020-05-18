API 문서 안내
===

API 문서는 Natural-JS 의 컴포넌트와 라이브러리에서 지원하는 기능과 옵션에 대한 사용법과 설명을 제공하는 문서입니다.

문서는 컴포넌트 별로 페이지가 분리 되어 있고 페이지 단락은 탭으로 구분 되어 있습니다.

* __개요__ : 컴포넌트나 라이브러리에 대한 개요.

* __API DEMO__ : 컴포넌트나 라이브러리를 실시간으로 테스트 할 수 있는 데모 프로그램

* __생성자__ : 컴포넌트나 라이브러리의 인스턴스를 생성할 때 실행되는 기능과 생성자 arguments 에 대한 설명.

    예) __N.grid__[<sup>1)</sup>](#fn1)(___argument[0]___[<sup>2)</sup>](#fn2)), __N().grid__(___argument[0]___)

* __기본옵션__ : 컴포넌트나 라이브러리의 기본 옵션에 대한 설명.

    예) N([]).grid(__{ resizeable : true }__[<sup>3)</sup>](#fn3))

* __선언형옵션__ : 컴포넌트나 라이브러리에서 사용하는 템플릿 HTML 요소들의 data-* 속성에 JSON 형태의 문자열로 정의 되는 옵션.

    예) &lt;input id="date" type="text" __data-format='[["date", 8]]'__[<sup>4)</sup>](#fn4) /&gt;

    * 선언형 옵션은 다음과 같은 속성으로 정의 할 수 있습니다.
        1. 포멧 룰(Format Rules) : data-format
        2. 검증 룰(Validation Rules) : data-validate
        3. a 와 b 를 제외한 모든 컴포넌트 옵션 : data-opts

<p class="alert">선언적 옵션은 JSON 표준 형식을 정확하게 준수해야합니다 (예 : 키 값은 큰 따옴표로 묶어야합니다). JSON 표준 포멧을 지키지 않으면 선언형 옵션이 인식되지 않거나 오류가 발생합니다.</p>

<div class="alert">
    data-format 이나 data-validate 등 선언형 옵션으로 실행되는 룰은 배열 형태의 문자열로 정의하고 룰명 다음에 인자들을 순서대로 나열 합니다.
    <div class="alert">예) data-format='[["date", 8], ["lpad", 10, "@"]]'</div>
</div>

* __함수__ : 컴포넌트나 라이브러리 인스턴스에서 제공하는 메서드와 arguments 에 대한 설명

    예) N([]).grid( { resizeable : true } ).__revert__[<sup>5)</sup>](#fn5)(__3__[<sup>6)</sup>](#fn6))

* __예제__ : 컴포넌트나 라이브러리 사용 예제

---

__용어__
* jquery object : jQuery() 나  $(), N() 함수를 실행 했을때 반환되는 jQuery 확장 객체 나 jQuery selector.
* selector : jQuery 에서 CSS selector 폼으로 지정하는 문자열이나 object, array, html element, function 등.

---

__주석__
1. <span id="fn1">생성자</span>
2. <span id="fn2">생성자 arguments</span>
3. <span id="fn3">기본옵션</span>
4. <span id="fn4">선언형옵션</span>
5. <span id="fn5">함수</span>
6. <span id="fn6">함수 arguments</span>