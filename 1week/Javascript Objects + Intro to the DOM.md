<h2> JS Objects + Intro to the DOM </h2>

<h4>4/10/14 // Afternoon //  Jen + Hannah</h4>

<h5> JS Objects </h5>

Structure & syntax of a Javascript object

	
	var lightsaber = { 
		color = "red",
		owner = "Count Dooku"
		};
	
	
**Google Chrome Console**
	
	lightsaber.color = "red" ;
	"red"
	var red = "the color red";
	undefined
	lightsaber.color = "red";
	"red"
	lightsaber
	Object {color: "red"}
	red
	"the color red"
	lightsaber.owner = "Count Dooku"
	"Count Dooku"
	lightsaber
	Object {color: "red", owner: "Count Dooku"}
	
	------------------------------------------------------------------------
	
	var vader = { name: "Darth Vader" }
	undefined
	vader
	Object {name: "Darth Vader"}
	vader.level = "Master"
	"Master"
	vader
	Object {name: "Darth Vader", level: "Master"}
	vader["jedi"]= false;
	false
	vader
	Object {name: "Darth Vader", level: "Master", jedi: false}
	
	------------------------------------------------------------------------
	// use delete luke.mom to delete a property
	
	luke
	Object {name: "Luke Skywalker", jedi: false, level: "Boss", age: 16, dad: "Darth Vader"…}
	age: 16
	dad: "Darth Vader"
	jedi: false
	level: "Boss"
	mom: "Natalie Portman"
	name: "Luke Skywalker"
	__proto__: Object
	delete luke.mom
	true
	
	luke
	Object {name: "Luke Skywalker", jedi: false, level: "Boss", age: 16, dad: "Darth Vader"}

<br />
	
<h6> Function </h6>

**'this' keyword** - Hard to describe and understand at first. 

	function Jedi(name,agility, wisdom, lightsaber){
	this.name = name; 
	this.agility = agility;
	this.speed = 150; 	this.wisdom = wisdom;
	this.lightsaber = lightsaber;
	}
	
	//even though speed is not coming from our argument, it's ok

**Chrome Console:**
	
	var luke = new Jedi("Luke Skywalker", 42, 0, "blue")
	undefined
	luke
	Jedi {name: "Luke Skywalker", agility: 42, speed: 150, wisdom: 0, lightsaber: "blue"}
	
	// Skips over speed because it has already been assigned.
	
*Try this out with Leia by only assigning her a name.*

	var leia = new Jedi("Leia Organa")
	undefined
	leia
	Jedi {name: "Leia Organa", agility: undefined, speed: 150, wisdom: undefined, lightsaber: undefined}
	
	
*Doesn't define any properties for her. If you update new objects for her, it wouldn't last for other new Jedi's because she isn't from the original function.*

**Show Keys of the object**

	var vader = new Object()
	undefined
	vader.name = "Darth Vader"
	"Darth Vader"
	vader.affiliation = "Sith"
	"Sith"
	vader.lightsaber = "red"
	"red"
	vader
	Object {name: "Darth Vader", affiliation: "Sith", lightsaber: "red"}
	Object.keys(vader)
	["name", "affiliation", "lightsaber"]
	
	for (i in vader) { console.log(vader[i]);}
	Darth Vader VM1561:2
	Sith VM1561:2
	red 
	
*For in loop*

	for (i in vader) {
	console.log (i + ": " + vader[i])
	};
<br />
<h4>DOM: Document Object Model</h4> 
It's an API in that sense that it's an interface between your document and your javascript. So you can just "change stuff."


	document
	
	document.styleSheets
	StyleSheetList {0: CSSStyleSheet, 1: CSSStyleSheet, length: 2, item: function}

	document.getElementsByTagName("p")
	
	document.getElementsByTagName("p")[0]
	
	document.getElementsByTagName("p")[0].innerHTML = "More pizza!"
	
	document.getElementsByClassName("lightsaber")
	
	document.getElementById("luke")
	
	document.getElementById("luke").style.display
	
	document.getElementById("luke").style.display = "block" // shows green light saber		
		
<h3>Assignment: Go wild and change the site however you want! Do it through the console! Have fun and eat more pizza!!
		
	
	
	
	
	