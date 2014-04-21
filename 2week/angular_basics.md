##Angular Basics
####4.15.14 // Afternoon // Lorin

<br />
####x-ng-app // x-ng-init
`Making the initial 3 x 3 boxes`

	<html>
	<head>
		<title></title>
		<style>
		div div{float:left; border:3px solid white; width:100px; height:100px; background-color:blue; color:white; font-size:15pt;}
		.row{clear:both;}
		</style>
	
		<script src="http://ajax.googleapis.com/ajax/libs/angularjs/1.2.15/angular.min.js"></script>
	</head>
	<body x-ng-app="" x-ng-init="rows = [1,2,3]; alert('hi'); ">
		<div class="row" x-ng-repeat="r in rows">
			<div></div>
			<div></div>
			<div></div>
		</div>
	
	
	</body>
	</html>
	
	

**$scope **- allows us to hold values temporarily. It's a way that the view and the controller can interact. The Scope is a view model.

**$index**  - how we can have things uniquely identified. Counting from 0. 

	<div class="row" x-ng-repeat="r in rows">
	<div>{{ r }}</div>
	<div>{{ 'x' }}</div>
	<div>{{ $index }}</div>
	</div>

**Chrome Console**

	angular
		- Object...
	document.getElementsByTagName("div") //how many divs are there?
	
	document.getElementsByTagName("div")[2]
		- <div class=​"ng-binding">​x​</div>​
		

`This is the way to see the scope: (btw almost no angular devel;oper knows about this!)`

	var myDiv = document.getElementsByTagName("div")[2]
	
`Note that the "2" finds the third DIV on the page`
		
		angular.element(myDiv).scope()
		
		

