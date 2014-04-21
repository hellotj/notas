<h2> JavaScript Scope </h1>

<h4>4/11/14 // Morning //  Jen + Mer</h4>

**Global Variable**
	
	var tRex = "Tyrannosaurus Rex";

**Local Variable**

	function clone(dino) {
		var d = dino;
		console.log(d + " " + d);
	}
	
	clone(tRex);
	Tyrannosaurus Rex Tyrannosaurus Rex
	
***

Global variable... You have to use parens () to be able ot run the function

	var dinosaur = "lady";
	var chaosTheory = function() {
	dinosaur = "mom"; //life finds a way
	console.log(dinosaur);
	}
	
	chaosTheory()
	mom
	
	dinosaur;
	"mom" 
	

	var securitySystem = {
	fences: "enabled",
	electrified: true,
	linesOfCode: 2000000,
	crash: function() {
	  var status = "down";
	  this.fences = "disabled";
	  alert("The fences are " + status + "!");
	}
	}
	
	//object, given properties, defined function called crash. This shows how objects are different than hashes. When we call crash, we'll expect a new var called status, then we'll disable fences, then we'll get an alert. 
	
	securitySystem.crash()
	

<h5>Context</h5>
	
*Using 'this' and functions to turn the program off and on. Notice reboot vs. crash. When it's crash then the alert says the fences are down and reboot says that JP is back online. *

**//From now on using double stars means the return from Chrome Console**

	var securitySystem = { 
	  fences: "enabled", 
	  electrified: true, 
	  linesOfCode: 2000000, 
	  crash: function() {
	    var status = "down";
	    this.fences = "disabled";
	    this.electrified = false;
	    tRex = "escaped";
	    alert("The fences are " + status + "!");
	},
	  reboot: function() {
	   this.fences = "enabled";
	   this.electrified = true;
	   tRex = "back in the paddock";
	   alert("Jurassic Park is back online.");
	}
	}
	**undefined**
	securitySystem.crash()
	**undefined**
	securitySystem.reboot()
	**undefined**
	tRex
	**"back in the paddock"**	
	securitySystem
	**Object {fences: "enabled", electrified: true, linesOfCode: 2000000, crash: function, reboot: function}**
	
	
