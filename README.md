<html>
<head>
<title>HTML Calculator</title>
</head>
<body bgcolor= "#000000" text= "gold">
<form name="calculator" >
<input type="button" value="1" onClick="document.calculator.ans.value+='1'">
<input type="button" value="2" onClick="document.calculator.ans.value+='2'">
<input type="button" value="3" onClick="document.calculator.ans.value+='3'"><br>
<input type="button" value="4" onClick="document.calculator.ans.value+='4'">
<input type="button" value="5" onClick="document.calculator.ans.value+='5'">
<input type="button" value="6" onClick="document.calculator.ans.value+='6'">
<input type="button" value="7" onClick="document.calculator.ans.value+='7'"><br>
<input type="button" value="8" onClick="document.calculator.ans.value+='8'">
<input type="button" value="9" onClick="document.calculator.ans.value+='9'">
<input type="button" value="-" onClick="document.calculator.ans.value+='-'">
<input type="button" value="+" onClick="document.calculator.ans.value+='+'"><br>
<input type="button" value="*" onClick="document.calculator.ans.value+='*'">
<input type="button" value="/" onClick="document.calculator.ans.value+='/'">

<input type="button" value="0" onClick="document.calculator.ans.value+='0'">
<input type="reset" value="Reset">
<input type="button" value="=" onClick="document.calculator.ans.value=eval(document.calculator.ans.value)">
<br>Solution is <input type="textfield" name="ans" value="">
</form>
</body>
<<<<<<< HEAD
</html>
=======
<!-- for styling -->
<style>
.title{
border-radius: 10px;
margin-bottom: 10px;
text-align:center;
width: 500px;
color:#ff4456;
border: solid black 1px;
}
input[type="button"]
{
border-radius: 10px;
background-color:#ff4456;
color: black;
border-color:#ff4456 ;
width:100%;
}
input[type="text"]
{
border-radius: 10px;
text-align: right;
background-color:white;
border-color: black ;
width:100%
}
</style>
>>>>>>> 3ab041dd5806a1bd26fe8fdf5e22f687973a9542
