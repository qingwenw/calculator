<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
	</head>
<body>

<form>
first number:<br>
<input type="text" id="num1">
<br>
second number:<br>
<input type="text" id="num2">
<br>
result here:<br>
<p id="result"></p>
<br>
</form>

<button id = "add">+</button>
<button id = "minus">-</button>
<button id = "multiply">*</button>
<button id = "divide">/</button>

<script src= "https://apps.bdimg.com/libs/jquery/2.1.4/jquery.min.js"></script>
<script>

//定义两个全局变量：

var a_int;
var b_int;

//为按钮添加事件：
$('#add').click(function(){
	gn();
	var result = addition(a_int, b_int);
	$('#result').html(String(result));
});

$('#minus').click(function(){
	gn();
	var result = subtraction(a_int, b_int);
	$('#result').html(String(result));
});

$('#multiply').click(function(){
	gn();
	var result = multiplication(a_int, b_int);
	$('#result').html(String(result));
});

$('#divide').click(function(){
	gn();
	var result = division(a_int, b_int);
	$('#result').html(String(result));
});

//获取两个变量的值并转化为数字：
function gn(){
	var a = $('#num1').val();
	var b = $('#num2').val();
	a_int = parseInt(a, 10);
	b_int = parseInt(b, 10);
}

function addition(x,y){
	return x + y;
}

function subtraction(x,y){
 	return x - y;
}

function multiplication(x,y){
	return x * y;
}

function  division(x,y){
	if (y == 0){
		alert("never give up hope:)");
		return;
	} else {
		return x / y;
	}
}
		</script>
</body>
</html>








