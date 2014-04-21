<h2>JavaScript Arrays + Loops </h2>
<h4>4/10/14 // Afternoon //  Marc + Mer</h4>


**Code is run in the Chrome Console**

`Regular (Slowest) way to make an array`

	var food=new Array();
	food[0]= "French Fries"
	"French Fries"
	food[1]= "Pizza"
	"Pizza"
	food[2]= "Donuts"
	"Donuts"
	food
	["French Fries", "Pizza", "Donuts"]

`Condensed (faster) way to make an array`
		
	var people=new Array("Jess","Lorin","Marc");
	people
	["Jess", "Lorin", "Marc"]
	
`Literal (fastest) way to make an array`
	
	var animals=["cat","dog","panda"];
	animals
	["cat", "dog", "panda"]
	

`Edits you can make`

	animals[2]="hippo";
	"hippo"
	animals
	"cat", "dog", "hippo"
	animals[4]="panda"
	"panda"
	animals
	["cat", "dog", "hippo", undefined × 1, "panda"]
	

`Pop + Push + Splice`

	animals.pop();
	"panda"
	animals.push();
	4
	animals.push("unicorn");
	5
	animals
	["cat", "dog", "panda", "horse", "unicorn"]
	animals.length
	5
	animals.splice(2,0,"squirrel","turtle");
	[]
	animals
	["cat", "dog", "squirrel", "turtle", "panda", "horse", "unicorn"]
	
`JS For Loops`

for(assignment; end condition; increment/decrement) { loop action }

	// Incrementing For Loop

	for(var i = 0; i< people.length; i++){
		console.log("The element at index " + i + "is: " + people[i]);
	} 
	
	//you don't have to use 'i', you can use anything but 'i' is common practice.

	console.log("This is a For Loop:");for(var i = 0; i< people.length; i++){
	console.log("The element at index " + i + "is: " + people[i]);
		} 
	This is a For Loop: VM1062:2
	The element at index 0is: Jess VM1062:3
	The element at index 1is: Lorin VM1062:3
	The element at index 2is: Marc 
	
	// Decrementing For Loop
	
	var mixed=[1, "two", "three", true];
	console.log("Decrementing For Loop");
	
	for(var i = mixed.length -1; i >= 0; i--){
		console.log("The element at index " + i + " is " + mixed[i]);
	}


`JS While Loops`

The condition needs to be true so that it continues to happen. 


while(condition) {
	code to be executed
	}
	
	// While Loop (with an alert)
	
	var veggies=["Asparagus", "Brussel Sprouts", "Kale", "Broccoli"];
	
	var i=0;
	while (veggies[i]){
		alert(veggies[i]);
		i++;
	}
	
	----------------------------------------------------------------------------------------
	// Demonstrating document.write, which writes it to the html. 
	
	var veggies=["Asparagus", "Brussel Sprouts", "Kale", "Broccoli"];
		
	var i=0;
	while (veggies[i]){
		document.write(veggies[i]); 
		i++;
	}


`Doing the last while loop as a for loop`

	for(var i=0; veggies[i]; i++){
		console.log(veggies[i]);
	}


<h5>Lab //</h5>  Create a button with just one loop, an html sheet, a CSS sheet and when you click it you receive an alert that cycles through an array.















	