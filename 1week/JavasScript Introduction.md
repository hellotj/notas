<h2>Javascript Intro - April 10</h2>

<h3>Useful Websites</h3>
**jshint.com** [check to see if you have issues in your code]

**codepen.com** [code with several languages at a time]



<h4>Introduction</h4>

1. Variables
2. Pojo's
3. Simple Functions
4. alerts
5. console.log()
6. brining in scripts 

Don't confused Java with Javascript!!! It's the ultimate newb thing to do. Java powers Android, it's totally different. 

Java is influenced the most *powerful* language, which is C.

> If it takes 50 lines of code to do something in C, Ruby can do it in just a few lines to do the same thing. 

If you can understand javascript, you could understand C and could be a segway to another field. 

[Franck's drawing of role of Javascript vs. others](http://i.imgur.com/7vOaAkf)


**Programming Styles**

* Object oriented //  don't do well when it comes to server farms.

`First JavaScript we did in Inspect Element`

    var room2 = {}
	undefined
	var room1 = {students: 20, name: "classroom1}
	SyntaxError: Unexpected token ILLEGAL
	room1
	ReferenceError: room1 is not defined
	var room1 = {students: 20, name: "classroom1"}
	undefined
	room1
	Object {students: 20, name: "classroom1"}
	room1.students
	20
    

**JSON - JavaScript Object Notation**

Twitter uses it, every big application. It's data coming over the wire coming into your application. 

`Trying out our first program about airlines. Javascript Code`

	var flight = {
  	airline: "Delta",
 	 number: 357, 
  	departure: {
    time: "2005-09-22 14:55",
    city: "Santa Monica"
  		},
  	arrival: {
  	airport: "LAX",
    time: "2005-09-22 14:57",
    city: "Los Angeles"
  		}
	};

	document. getElementById("AirlineName").innerHTML=flight.airline; 

	// innerHTML transfers the html data to JS. getElementbyID is a method that the document supports. If you do class instead of Id it would be .getElementsByClass and it would return an array.


	document.getElementById("FlightNumber").innerHTML=flight.number;
	document.getElementById("DepartureCity").innerHTML=flight.departure.city;
	document.getElementById("DepartureTime").innerHTML=flight.departure.time;


`Flight Program: HTML`

	<h2>My Flight Information</h2>
	<p>
  	Airline Name: <span id="AirlineName"></span><br />
  	Flight Number: <span id="FlightNumber"></span><br />
  	Departure City: <span id="DepartureCity"></span><br />
  	Departure Time: <span id="DepartureTime"></span><br />
	</p>
	
	
	
`Final Javascript code entered in sublime`

	
	
	var flight = {
	  airline: "Delta",
	  number: 357,
	  departure: {
	    time: "2005-09-22 14:55",
	    city: "Santa Monica"
	  },
	  arrival: {
	    time: "2005-09-22 14:57",
	    city: "Los Angeles"
	  }
	};
	
	document.getElementById("AirlineName").innerHTML=flight.airline;
	
	// innerHTML transfers the html data to JS. getElementbyID is a method that the document supports. If you do class instead of Id it would be .getElementsByClass and it would return an array.
	console.log(flight.number);
	
	document.getElementById("FlightNumber").innerHTML=flight.number;
	document.getElementById("DepartureCity").innerHTML=flight.departure.city;
	document.getElementById("DepartureTime").innerHTML=flight.departure.time;


`HTML code that calls that Javascript`


	<head>
	</head>
	
	<body>
	
	<h1>Flight Program</h1>
	
	<p>
	  Airline Name: <span id="AirlineName"></span><br />
	  Flight Number: <span id="FlightNumber"></span><br />
	  Departure City: <span id="DepartureCity"></span><br />
	  Departure Time: <span id="DepartureTime"></span><br />
	</p>
	  <script src="js/script.js"></script>
	</body>
		