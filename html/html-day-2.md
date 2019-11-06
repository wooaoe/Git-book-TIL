# HTML Day 2

> HTML 링크 관련 태그

```markup
<!DOCTYPE html>
<html> 
<head>
<meta charset="UTF-8">
<title>링크</title>
</head>
<body>
<h1>하이퍼링크 관련 태그</h1>
	<!--a태그의 href 속성으로 링크를 만들 수 있다. -->
	<h3>a태그를 이용한 하이퍼링크 테스트</h3>
	<ul>
		<li><a href = "test.html">test.html</a></li>
		<li><a href = "html01_block_inline.html">html01</a></li>
		<li><a href = "html2_title_paragraph.html">html2</a></li>	
	</ul>
	<br/>
	
	<h3>웹페이지 링크 테스트</h3>
	<ul>
		<li><a href = "http://www.naver.com" target = "_blank">네이버</a></li>
		<!--target = "_blank"를 하게 되면 새탭에서 페이지가 열림 -->
		<!--target = "_self"==default : 기존 탭에서 페이지가 열림 -->
		
		<li><a href = "http://www.google.com" target = "_blank">구글</a></li>
		<li><a href = "http://www.instagram.com" target = "_self">인스타그램</a></li>
		<li><a href = "http://www.29cm.com" target = "_blank">29cm</a></li>	
		
	</ul>

	<br/>
	<h3>페이지 내에서 링크를 통한 이동</h3>
	<ul>
		<li><a href = "#a">1번으로</a></li>
		<li><a href = "#b">2번으로</a></li>
		<li><a href = "#c">3번으로</a></li>
		<!-- #a, #b, #c : id와 구별하기 위해 #을 붙여줌 / 링크 맨 뒤에 #a, #b, #c 이렇게 붙음 -->	
	
	</ul>
	
	<br><br><br><br><br><br><br>
	<br><br><br><br><br><br><br>
	<br><br><br><br><br><br><br>
	<br><br><br><br><br><br><br>
	<br><br><br><br><br><br><br>
	<br><br><br><br><br><br><br>
	<br><br><br><br><br><br><br>
	<br><br><br><br><br><br><br>

<p id = "a">1번</p>

	<br><br><br><br><br><br><br>
	<br><br><br><br><br><br><br>
	<br><br><br><br><br><br><br>
	<br><br><br><br><br><br><br>
	<br><br><br><br><br><br><br>
	<br><br><br><br><br><br><br>
	<br><br><br><br><br><br><br>
	<br><br><br><br><br><br><br>
	
<p id = "b">2번</p>

	<br><br><br><br><br><br><br>
	<br><br><br><br><br><br><br>
	<br><br><br><br><br><br><br>
	<br><br><br><br><br><br><br>
	<br><br><br><br><br><br><br>
	<br><br><br><br><br><br><br>
	<br><br><br><br><br><br><br>
	<br><br><br><br><br><br><br>

<p id = "c">3번</p>

	<br><br><br><br><br><br><br>
	<br><br><br><br><br><br><br>
	<br><br><br><br><br><br><br>
	<br><br><br><br><br><br><br>
	<br><br><br><br><br><br><br>
	<br><br><br><br><br><br><br>
	<br><br><br><br><br><br><br>
	<br><br><br><br><br><br><br>
	
	<p></p>
	<!--<p></p>를 뒤에 붙여주면 공백을 제거하고 3번을 보여줌-->

</body>
</html>
```

> HTML 표 관련 태그

```markup
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>테이블</title>
</head>
<body>
<!-- 
	<table> : 기본적인 표를 생성해주는 태그
	<tr> : 표의 행을 나타내는 태그
	<th> : 표의 제목 셀을 나타내는 태그
	<td> : 표의 일반 셀을 나타내는 태그 

 -->

<h2>기본 테이블 만들기</h2>
<table border = "1" style = "width : 300px">
	<tr style = "background-color : gray">
		<th>cloumn01</th>
		<th>cloumn02</th>	
	</tr>
	<tr>
		<td>1</td>
		<td>2</td>	
		
	</tr>
	<tr>
		<td>3</td>	
		<td>4</td>
	</tr>

</table>
<br/>
<br/>
<br/>

<table border = "1">
	<caption>테이블 제목</caption>
	<colgroup>
		<col width = "100px"/>
		<col width = "200px"/>
		<col width = "300px"/>	
	</colgroup>
	
	<thead>
		<tr style = "background-color : pink">
			<th>컬럼1</th>
			<th>컬럼2</th>
			<th>컬럼3</th>
		</tr>
	</thead>
	
	<tbody>
		<tr>
			<td>내용1</td>
			<td>내용2</td>
			<td>내용3</td>		
		</tr>
	</tbody>
	
	<tfoot>
		<tr>
			<td>내용4</td>
			<td>내용5</td>
			<td>내용6</td>		
		</tr>	
	</tfoot>

</table>

<h3>테이블 셀 병합하기</h3>
<!-- 
	<td>태그의 속성을 이용해서 행과 열을 합칠 수 있다.
	<colspan> : 열 합치기
	<rowspan> : 행 합치기 
 -->
<table border = "1">
	<caption>테이블 병합</caption>
	<thead style = "background-color : pink">
		<tr>
			<th>컬럼1</th>
			<th>컬럼2</th>
			<th>컬럼3</th>
			<th>컬럼4</th>
		</tr>
		
	</thead>
	
	<tbody>
		<tr>
			<td rowspan = "2">1[세로 합침]</td>
			<td>2</td>
			<td>3</td>
			<td>4</td>		
		</tr>
		<tr>
			<td colspan = "2">5[가로 합침]</td>
			<td>6</td>
			<td>7</td>
			<td>8</td>		
		</tr>
	</tbody>

	<tfoot>
		<tr>
			<td colspan = "6">가로 전부 합치기</td>		
		</tr>	
	
	</tfoot>

</table>


</body>
</html>
```

> HTML  이미지 관련 태그

```markup
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>이미지 관련 태그</title>
</head>
<body>
<!-- 이미지 삽입하기 위한 <img>태그 사용
	파일의 경로 : src이라는 속성
	<img>태그는 닫기 태그 사용X
 -->
 
<h1>이미지 관련 태그</h1>
	<img src = "sample/image/river1.PNG">
	<p>src 속성 경로를 세팅하여 파일을 불러온다.</p>
<hr/>

	<h2>자주 사용되는 속성</h2>
	<h3>alt 속성</h3>
	<p>이미지를 읽어올 수 없을 경우 대체되는 텍스트</p>
	<img alt="강 사진" src="sample/image/river1.png">
<br/>
	<h3>width와 height 속성</h3>
	<h4>고정 크기 : 화면의 사이즈가 바뀌어도 크기가 변하지 않는다.</h4>
	<img src = "sample/image/flower1.PNG" width = "200px" height = "150px">
	<img src = "sample/image/flower2.PNG" width = "200px" height = "150px">
	<img src = "sample/image/flower3.PNG" width = "200px" height = "150px">
	<br/>
	<img src = "sample/image/flower4.PNG" width = "200px" height = "150px">
	<img src = "sample/image/flower5.PNG" width = "200px" height = "150px">
	
	<hr/>
	<h4>가변 크기 : 화면의 사이즈가 바뀌면 크기도 변한다.</h4>
	<img src = "sample/image/flower1.PNG" width = "15%" height = "150px">
	<img src = "sample/image/flower2.PNG" width = "15%" height = "150px">
	<img src = "sample/image/flower3.PNG" width = "15%" height = "150px">
	<br/>
	<img src = "sample/image/flower4.PNG" width = "15%" height = "150px">
	<img src = "sample/image/flower5.PNG" width = "15%" height = "150px">
	<hr/>
	
	<h4>이미지 구역을 2개로 나누어 각각 링크를 설정</h4>
	<img src = "sample/image/river1.PNG" usemap = "#map">
	<!--map 태그로 이미지 맵을 만든다.(이미지맵이란 클릭을 할 수 있는 영역) -->
	<map name = "map">
		<area shape = "rect" coords = "00,00,300,500" href = "http://www.naver.com" target = "_blank">
		<!-- 00,00,300,500으로 맞춰주면 왼쪽에만 설정됨 -->
		<area shape = "rect" coords = "300,00,628,419" href = "http://www.google.com" target = "_blank"                >
		
	
	</map>

</body>
</html>
```

> HTML 미디어 관련 태그

```markup
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>미디어</title>
</head>
<body>
	<h3>오디오 태그</h3>
	<audio src="sample/audio/major.mp3" controls = "controls" autoplay = "autoplay"></audio>
	<h3>비디오 태그</h3>
	<video src="sample/video/video1.mp4" controls = "controls"></video>
	<h3>iframe</h3> <!--페이지 내 다른 페이지 불러올 수 있음(유투브, 또는 문서 등) -->
	<iframe src = "https://www.youtube.com/embed/2KtFPjSp3og" frameborder = "5" gesture = "media" allow = "encrypted-media"
		allowfullscreen></iframe>


</body>
</html>
```

> HTML form 관련\(input, fieldset\) 태그

```markup
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>form01</title>
</head>
<body>
	<form action = "html12_form01_res.html" method = "get">
	<!-- 
		전송(submit)을 눌렀을 때 action에서 지정해준 경로(#)를 통해 method에 지정한 방식(get)으로
			 input 태그의 값이 전달된다. 
		action : form 태그에 입력된 값을 전송받을 서버의 클래스명을 지정하는 태그(수신대상)
		method : get(입력된 값들을 주소에 포함시켜 전달)/post(입력된 값들을 숨겨서 주소를 전달)로 전송방식을 지정(전송방식) 
		
	 -->
		<!-- <label>검색할 내용 :</label>
		<input type = "text" size = "15" name = "search"> <input type = "submit" value = "search">-->
		
		<fieldset> <!--html 요소(p, input 등등)를 박스로 묶어주는 태그
					<legend> : 필드셋의 제목을 정해주는 태그 -->
			<legend>회원가입</legend>
		<p>아이디 : <input type = "text" name = "ID" placeholder = "id"/></p>
		<p>비밀번호 : <input type = "password" name = "Pwd" placeholder = "password" /></p>
		<p>이메일 수신 여부
			<input type = "radio" name = "radio" value = "y"/> 동의
			<input type = "radio" name = "radio" value = "n"/> 거부
		</p>
		
		<p>관심분야
			<input type = "checkbox" name = "cb1" value = "달빛조각사" />달빛조각사
			<input type = "checkbox" name = "cb2" value = "스포츠토토" />스포츠토토
			<input type = "checkbox" name = "cb3" value = "신분증재발급" />신분증재발급		
		
		</p>
		
		<p>
			<input type = "submit" value = "가입하기"/>
			<input type = "reset" value = "취소"/>
			<input type = "button" value = "버튼"/>
		</p>
		
		<p>
			<input type = "file"/>
			<input type = "hidden" name = "hidden01" value = "my_hidden_value"/>
			<!--페이지에서 주소를 넘겨줄 때 hidden을 사용해서 가려줌 (사용자에게는 안뜸)-->
		
		</p>

		</fieldset>
	</form>

</body>
</html>
```

> HTML  form 관련\(legend, label, select, option, optgroup\) 태그

```markup
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>form02</title>
</head>
<body>
<h1>select 요소</h1>
<form action = "html12_form01_res.html" method = "get">
	<fieldset>
		<legend>여러줄 글상자와 목록상자</legend>
		<p>
			<label>답글</label><br/>
			<textarea rows = "5" cols = "100" name = "ta"></textarea>		
		</p>
		
		<p>
			<input type = "submit" value = "전송"/>
		</p>
		
		<p>
			<select name = "selected01">
				<option value = "html">HTML</option>			
				<option>CSS</option>			
				<option>JS</option>			
				<option>JQuery</option>			
			</select>
		</p>
		
		<p>
			<select name = "select02">
				<optgroup label="서울"></optgroup>
					<option value = "gang-nam">강남</option>
					<option value = "sadang">사당</option>
					<option value = "gu-ro">구로</option>
				
				<optgroup label="경기"></optgroup>
					<option value = "su-won">수원</option>
					<option value = "an-yang">안양</option>
			</select>
		</p>
	
	
	</fieldset>

</form>



</body>
</html>
```

