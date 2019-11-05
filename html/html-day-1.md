# HTML Day 1

* [ ] 블록요소와 인라인 요소 태그

```markup
<!DOCTYPE html>
<!--언어 버전 정하는 부분 -->
<html>
<head>
<meta charset="UTF-8">
<title>블록요소 인라인 요소</title>
<!-- 블록안의 또 다른 요소 == 인라인 요소 -->
</head>
<body>
	<h2>블록 요소</h2>
	<p>줄바꿈</p>
	
	<!--블록이 나뉘어져서 줄 바꾸기 가능 -->
	<div style="background-color: pink">
		블록 요소 안에 텍스트, <strong>인라인 요소</strong> 포함 가능
		<p>블록요소 안에 블록요소도 포함 가능</p>
	</div>
	<!--전체적인 레이아웃을 잡아주는 기능(구역을 나누어주는 것) ex)메뉴구현-->
	<h2>블록 요소2</h2>
	<p>HTML이란?</p>
	<blockquote>
		<!--인용하는 글을 적을 경우 사용함 ex)blockquote -->
		Hypertext Markup Language is the standard markup language for
		documents designed to be displayed in a web browser. It can be
		assisted by technologies such as Cascading Style Sheets and scripting
		languages such as JavaScript
	</blockquote>
	<p>
		속담에 <q><strong>가는 말이 고와야 오는 말이 곱다.</strong></q>라는 속담이 있습니다.
		<!--""달아주는 태그 ex) <q> -->
	</p>

	<h2>인라인 요소</h2>
	<a>줄바꿈 X </a>
	<!-- 줄바꿈 태그 : <br/> 사용하면 됨. -->
	<a>줄바꿈<br/>될까요? 되네요
	</a>
	<!--<a> : 하이퍼링크를 달아주는 태그 -->
	<br />

	<a href="http://www.naver.com">네이버</a>
	<a href="test.html">테스트</a>
	
	<q style = "background-color : skyblue">인라인 요소 안에 텍스트와<a> 인라인요소</a> 포함가능</q><br/>
	<span>인라인 요소 안에 <p>블록 요소</p> 포함 불가</span>
	<!--CSS랑 같이 쓰는 태그 : <span>-->
	<!--인라인 요소 안에는 블록 요소 되도록 사용하지 않기-->
</body>
</html>
```

* [ ] 글자 요소 태그 

```markup
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8"> <!--문서가 어떻게 구성되어 있는지에 대한 정보 태그 : <meta> -->
<meta name = "Generator" content = "Eclipse">
<!--Generator : 어디서 만들었는지(문서를 작성한 도구가 무엇인지) -->
<meta name = "Author" content = "개발자">
<!--Author : 누가 만들었는지 -->
<meta name = "Keywords" content = "">
<!--Keywords : 키워드 설정 ','를 통해 여러 단어 설정 가능 -->
<meta name = "Description" content = "">
<!--Description : 요약글(설명)을 나타내는 것 -->

<title>제목, 단락 태그</title>
</head>
<body> 
<!--h1 > h2 > h3 > ...순으로 글자 크기가 줄어듦 -->
<h1>제목</h1>
<h2>글자</h2>
<h3>크기</h3>
<h4>지정</h4>
<h5>하는</h5>
<h6>태그</h6>
	
<p>p 요소는 단락을 정의</p>
<div>div 요소는 영역을 정의</div>

<address>연락처 : 010-1234-5678</address>

</body>
</html>
```

* [ ] 텍스트 관련 태그

```markup
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>텍스트 관련 태그</title>
</head>
<body>

	<h1>h1 태그</h1>
	<h2>h2 태그</h2>
	<!-- 줄 바꿈 -->
	<br/>
	
	<!-- 글꼴 -->
	<h3>텍스트를 다루는 태그들</h3>
	일반글꼴
	<br/>
	<b>글자를 굵게 표시하는 태그</b>
	<br/>
	<strong>글자를 굵게 표시하는 태그</strong>
	<br/>
	<em>글자를 기울이는 태그</em>
	<br/>
	<i>글자를 기울이는 태그</i>
	<br/>
	<mark>형광펜 효과를 나타내는 태그</mark>
	<br/>
	<small>글자를 작게 표시하는 태그</small>
	<br/>
	기본 글자에<sub>아래 첨자</sub>를 나타내는 태그와 <sup>위첨자</sup>를 나타내는 태그이다.
	<br/>
	<s>글자에 취소선을 넣는 태그</s>
	<br/>
	
	<pre>
	입력한 형태 그대로 보여주는 태그 
	안녕하세요 
	저는                      재미있지 않아요.
	</pre>
	<hr/>
	<!--문단을 나누어주는 줄을 그어주는 태그 -->
	<!--<pre> : 상세한 설정을 해주기가 어려움 -->
	<br/>
	
	<h3>글자관련 태그 응용</h3>
	<p>태그들은 해당 태그 내에서 중첩으로 사용 가능하다.<br/>
	<strong>굵은</strong>글자를 사용할 수도 있고, <s>취소선</s>을 넣거나, <i>기울이는 등</i><br/>
	다양하게 사용할 수 있다.
	</p>
	
	<h2>셀프 연습</h2>
	<p>무엇을 연습해볼까요?</p>
	<div style = "background-color : orange">
	귤 먹고싶다 <q>귤</q> <br/>
	<strong>나는 귤을 좋아해!</strong>
	</div>
	
	
	
</body>
</html>
```

* [ ] 리스트 요소 태그

```markup
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>리스트</title>
</head>
<body>

	<h1>목록</h1>
	<h2>순차적 목록</h2>
	<p>학원 오는 순서</p>
	<ol>
		<li>눈을 뜬다.</li>
		<li>일어난다.</li>
		<li>씻는다.
			<ol type="i">
				<!-- i, I, a, A, 1 -->
				<li>양치한다.</li>
				<li>머리 감는다.</li>
			</ol>
		</li>
		<li>옷을 입는다.
			<ol type="1" start="5">
				<li>티셔츠를 입는다.</li>
				<li>바지를 입는다.</li>
				<li>코트를 입는다.</li>
				<li>신발을 신는다.</li>
			</ol>
		</li>
		<li>출발한다.
			<ol reversed = "reversed">
				<li>문을 연다.</li>
				<li>계단을 내려온다.</li>
				<li>지하철역으로 간다.</li>
				<li>지하철을 탄다.</li>
			</ol>
		</li>

	</ol>
	<hr />


	<h2>비 순차적 목록</h2>
	<b>집으로 가는 순서</b>
	<ul>
		<li>15:15까지 가방을 싼다.</li>
		<li>건물 바깥으로 뛰어 나간다.</li>
		<li>
			<ul>
				<li>정류장으로 간다.</li>
				<li>지하철역으로 간다.</li>
				<li>걸어간다.</li>
				<li>시동을 건다.</li>
			</ul>
		</li>
			<li>탈 것을 탄다.</li>
	
	</ul>
	
	<h2>정의형 목록</h2>
	<dl>
		<dt>(제목)학원 강의 시간</dt>
		<dd>오전시간</dd>
		<dd>점심시간</dd>
		<dd>오후시간</dd>
	</dl>

</body>
</html>
```

* [ ] 영역 관련 태그

```markup
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Insert title here</title>
</head>
<body>
	<!-- 영역 구분 짓는 태그
		<p> : 문단 영역을 지정(블럭 요소)
		<pre> : 입력한 대로 문단 영역 지정(블럭 요소)
		<div> : 줄바꿈이 적용 됨.
		<span> : 줄바꿈 적용 안됨.	
	 -->	
	
	<h1>영역 관련 태그</h1>
	<h3>div</h3> <!--줄바꿈을 통해서 영역이 지정됨 -->
		<div style = "background : pink; width : 100px; height : 100px;">처음</div>
		<div style = "background : red;">중간</div>
		<div style = "background : skyblue; width : 100px; height : 100px;">끝</div>
		<hr/>
	<h3>span</h3> <!--글자 영역만큼만 하이라이트 지정됨 -->
		<span style = "background : red;">처음</span>
		<span style = "background : green;">두음</span>
		<span style = "background : blue;">세음</span>
		<hr/>
</body>
</html>
```

