CSS Box Model
============================

Page elements are displayed and positioned according to a set of guidelines known as the "box model." Every element is treated as a rectangle consisting of four components -- the content, padding around it, a border that encompasses the element, and a margin that cushions the element.

*From the inside out:*

**Content** - the contents of the page element -- text, image, whatever's contained in that div, etc. 

**Padding** - the space between the content and the border  

**Border** - the border (visible or not) that defines the edges of the element (including things like background color)  

**Margin** - the space between the element and others on the page (think of it like a force field)


---

![image](images/boxmodel.png)

---

##Box Model Tips, Tricks, and Trivia

- With the exception of content, all of the box model properties can be set for the entire element or any number of sides. *Margin-top*, *border-left*, and *padding-right* (as well as other combinations of sides/properties) are all acceptable.
- You can set multiple sides at once with the generic property; instead of setting separate values for *margin-top* and *margin-right* and *margin-bottom* and *margin-left*, you might set ```margin: 5px 15px 30px 10px;``` (the order goes top, right, bottom, left). You can also set multiple sides with one declaration; ```margin: 5px 15px;``` will set the top and bottom margins to 5px and the left and right to 15px. (Three values would set individual top and bottom values, with left and right sharing the second value stated.)
- You may omit or set to 0 any of these properties; *margin: 0;*, *border-left: none;* or *padding-top* without defining padding for any other sides are both okay.
- Box model math includes more than you might expect! Setting a width or height on an element is just part of the equation; you also need to include right and left padding, border, and margin in your width calculation, and top and bottom padding, border, and margin in your height calculation. So, in this example:

```
    .container { 
     height: 100px;
     width: 100px;
     padding: 5px;
     border: 0px;
     margin-left: 20px;
     }
```

The height of the container might be 100px, but we're also dealing with 5px each of padding on the top and bottom, treating it like a 110px tall rectangle. The width might be declared as 100px, but that same 5px of padding on the left and right (+10px) and the extra 20px of margin on the left makes it occupy the same amount of space as a 130px wide rectangle. There's no border, so we don't have to factor it in this time.
