<h2>JS Objects</h2>
<h4> 4.11.14 // Morning // Lorin </h4>

**Outline**

* Review of referencing DOM
* Three ways to wire up events
* Mouse events [on mouse over, on mouse out, on mouse move]

**Referencing the DOM**

`HTML` 
	
	<!DOCTYPE html>

	<html>
	<head>
		<title>Don't step on the eye of the Iris!</title>
	
	
		<style>
		div{float:left; border:3px solid white; width:100px; height:100px; background-color:blue; color:white; font-size:15pt;}
		.row{clear:both;}
		</style>
	
	<script src="script.js"></script>
	</head>
	
	<body>
		<div id="myDiv"></div>
		
	</body>
	</html>
	
`JS`

	window.onload = function(){

	document.getElementById("myDiv").onclick = function(){
		this.style.backgroundColor = "#800A00"; //This is called an event handler
		};
	};
	
`Better JS way to do it by creating a variable and is passing a "delegate"`

	window.onload = function(){
	document.getElementById("myDiv").onclick = whenClicked; 
	};
	
	var whenClicked = function(){
		this.style.backgroundColor = "#800A00"; //This is called an event handler
	};
	
	
	
	
	