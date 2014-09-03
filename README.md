<!DOCTYPE html>
<html>
<head>
<meta charset="EUC-KR">
<title>Insert title here</title>
</head>
<body>
<input type = text id = "pivot" value=10 onchange="writePivot()" /> <br><br>

<input type = "text" id ="num1"/>+
<input type = "text" id ="num2"/>=
<span id="sum">10</span><br><br>

<button onclick = "init()">게임시작</button>
<button onclick = "exit()">게임종료</button>
<button onclick = "checkAnswer()">정답체크</button>
<p id="notice"></p>

<script>
var pivot = parseInt(document.getElementById("pivot").value);
var score = 0;
var cnt = 0;

function writePivot(){
	pivot=parseInt(document.getElementById("pivot").value);
	document.getElementById("sum").innerHTML=pivot;	
}
function checkAnswer(){
	
}
function init(){

}
function exit(){
	if(score!=0){
		document.getElementById("num1").value="";
		document.getElementById("notice").innerHTML=Math.ceil((score/cnt)*100)+"점";
	}
	cnt = 0;
	score = 0;
}
</script>

</body>
</html>
