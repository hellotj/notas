#Angular Directives

Directives are (1) one of the most critical elements to AngularJS and (2) often the most misunderstood. We're going to try to clear these up, and we'll practice using built-in Angular directives. (Custom directives == a specialized lesson we'll tackle near the end of the course.)

One way to think of directives is as **reusable web components**. Your content (as shown in the browser) is updated based on data. Directives are very flexible, and once you master how to use them, you can accomplish a great deal. It's one of the reasons we dig Angular so much!

**Best practice bonus:** directives with only one job are the most reusable, and therefore the most generally useful. For example, ```ng-repeat``` exists only to handle repetition, not anything else. We love that! [Insert ```you had ONE JOB!``` joke here.]

##Angular directives can…

- be used as HTML element attributes ```<div complete></div>```
- be used as HTML elements ```<complete></complete>```
- be used as class names ```<div class="complete"></div>``` // Not really used bc Microsoft doesn't work with it
- be used as comments ```<!-- directive: complete -->``` // Not used at all


**Best practice bonus:** it's recommended to focus on those first two (attributes and elements) and less on classes and comments. If there's a possibility that your users will be on older browsers (IE6 and such), avoid using element directives, too -- their custom element recognition is pretty abysmal.

##A quick syntax note about the hyphenated-words and camelCase

- hyphenated-words show up in the declaration, like so: ```<div i-am-a-directive</div>```
- camelCase is used in the directive definition, like so: ```App.directive('iAmADirective', function() {... });```

##Know your built-ins

Angular comes with several built-in directives. These are some key built-ins that you'll probably encounter fairly often (**in alphabetical order**):

- **ngApp / ng-app** -- bootstraps Angular onto your app // ***[Every angular app has to have this. Mostly common to use in the body. Only things inside will get the angular bootstrapped on.]***
- **ngBind / ng-bind** -- replaces contents of an HTML element with the value of the selected expression / updates when that expression changes // ***[don't have to put a piece of data, you can put an expression like a math equation. it doesn't have to be a string.]  $scopesomething = "2+2";, <div x-ng-bind = "something"></div>***
- **ngClass / ng-class** -- allows dynamic setting of classes on an HTML element via bound expression  
- **ngClick / ng-click** -- triggers a custom action (function) on click // ***won't have to use onclick anymore***
- **ngController / ng-controller** -- assigns the controller of your choice to a section of code //
- **ngModel / ng-model** -- binds an input (or other form controls, like select, textarea, etc) to a property on the scope
- **ngRepeat / ng-repeat** -- loops over a structure (like an array) and executes an instance of the selected code once per item ***// loops over a data structure like an array***
- **ngStyle / ng-style** -- conditionally sets style on an HTML element ***//basically like setting inline styles. you can call a function that will set your style***

####Angular is GREAT for SINGLE PAGE APPS

###### $SCOPE IS OUR MODEL. 















<BR />
<BR />
<BR />
<BR />
<BR />
<BR />
<BR />
<BR />
<BR />
<BR />
<BR />
<BR />
<BR />
<BR />
<BR />
<BR />
<BR />
<BR />
<BR />
<BR />



