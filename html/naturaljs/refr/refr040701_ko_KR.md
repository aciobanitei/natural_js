개요
===

Form(N.form) 은 context 옵션으로 지정한 요소(div, table 등의 block 요소)에 단건 로우 데이터를 바인드하거나 생성하는  UI 컴포넌트입니다.

<p class="alert">N.form 는 Natural-DATA 패키지의 컴포넌트들과 연동하여 데이터 포멧팅 및 입력 데이터의 유효성 검증 프로세스를 단순화 합니다. 자세한 내용은 [선언형옵션] 탭을 참고 해 주세요.</p>
<p class="alert">바인딩 된 데이터 오브젝트의 프로퍼티명(컬럼명)과 요소의 id 속성 값이 일치하면 데이터가 바인딩 됩니다. 데이터가 요소에 바인딩 되어야 데이터 포멧팅과 유효성 검증이 활성화 됩니다.</p>
<p class="alert">N.form 의 context 요소 안에 있는 요소를 N.form 이나 데이터 관련 컴포넌트(N.grid, N.list 등)의 context 로 다시 지정 하면 오류가 발생 하거나 데이터 동기화에 문제가 생길 수 있습니다. N.form 의 context 요소들을 중복 되지 않게 나누어 지정 하거나 컬럼 데이터가 중복 되지 않게 데이터를 나누어서 바인드 해야 합니다. context 요소나 데이터를 분리하는 방법은 예제 > <a href="#ZXhhcDA5MDAlMjQlRUIlQTklODAlRUQlOEIlQjAlMjAlRUQlOEYlQkMlMjAlRUIlQjAlOTQlRUMlOUQlQjglRUIlOTMlOUMkaHRtbCUyRm5hdHVyYWxqcyUyRmV4YXAlMkZleGFwMDkwMC5odG1s">멀티 폼 바인드</a> 메뉴의 소스 코드를 참고 바랍니다.</p>
<div class="alert">이미 생성 된 폼 요소에 add() 를 한 후 bind() 하거나 bind() 한 후 add() 또는 bind() 후 bind() 하면 폼의 입력 요소의 데이터 동기화 로직에 문제가 생길 수 있습니다. 이때는 반드시 중간에 unbind 메서드를 실행 해 주세요.
<pre style="margin-bottom: 0;"><code>var formInst = N([]).form().add();
formInst.unbind().bind(0, [{ "col01" : "abcd" }])</code></pre>
</div>
<p class="alert">입력요소의 값을 변경하거나 val 메서드로 데이터가 변경되면 rowStatus 프로퍼티가 생성되고 입력은 "insert", 수정은 "update", 삭제는 "delete" 값이 입력 됩니다.</p>