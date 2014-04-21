#CSS Specificity

###General Rules

- The closer to the HTML, the higher priority a rule has. (This means inline styles trump CSS rules, and also that rules lower down a stylesheet trump rules that modify the same property on the same selector.)
- **id** trumps class and element when it's a single selector.
- **class** trumps element when it is a single selector, but it's beaten by id.
- **element** is great for DRY code; set global styles and let other (more specific) selectors override. Let ids and classes handle the specifics!

###CSS Specificity Calculation

Sometimes, it helps to calculate specificity with math. An easy way to compare selector specificities is by assigning the following values for each:


| id (#) | class (.) | element |
|-------:|----------:|--------:|
| 100    | 10        | 1       |

**Simple example:**

```

	div { 
		color: red;
		}
	.blue { 
		color: blue;
		}
	#green { 
		color: green;
		}
		
	---------------------------	
		
	<div id="green" class="blue">What color is this text?</div>

```
In this simple example, 

- ```div``` has a specificity equal to 1, because it's an element.
- ```.blue``` has a specificity equal to 10, because it's a class.
- ```#green``` has a specificity equal to 100, because it's an id.

100 > 10 > 1, so our id (```green```) wins, and the text is green.

With single selectors, you're going to look at calculations that involve the digit ```1``` a lot; you'll see other digits once you start to bring nesting into the picture (i.e. ```p.blue a```, which has two elements -- ```p``` and ```a``` -- and a class, ```.blue```)


###Special Overrides

- **!important** is used to override the order of repeated rules.

```
	.container { 
		background-color: blue !important;
		background-color: grey;
		}
```
(in the sample above, blue would normally be overridden by grey because grey is listed after it, but the **!important** indicator prevents that override)

- **inline styles** touch the HTML directly, so they override CSS rules.

###Patterns We've Noticed

- ```!important``` trumps inline styles; it's the ultimate tiebreaker at the same-specificity level.
- ```!important``` can't do anything about styles outside of the element at-hand (i.e. you can't override a font color specified in a ```<p>``` from its parent ```<div>``` just by including ```!important```).
- Elements can have ids and classes together, and more than one class.
- It doesn't matter whether you declare an id or a class first (on a single element) in the HTML.
- It doesn't matter which order you list classes (on a single element) in the HTML.

###Battles

- **id** vs. **class** ----> id wins
- **element** vs. **class** ------> class wins
- **class** vs. **class** ------> last one declared on the stylesheet (of same rules) wins
- **id** vs. **nested element** (i.e. ```<div id="container">Here's our text</div>``` vs. ```<div id="container"><p>This text is in a p tag now</p></div>```) ------> the nested element wins, and the style rule for ```<p>``` is what sticks