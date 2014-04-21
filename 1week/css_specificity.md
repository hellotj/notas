#CSS Specificity
###General Rules
- The closer to the HTML, the higher priority a rule has
- **id** trumps class and alement when it's a single selector.
- **class** trumps element when it is a single selector, but it's beaten by id
- **element** is a great for DRY code; set gloabl styles and let other (more specfic) 

###Special Overrides
**!important** is used to overrisde the order of repeated rules.
**inline styles** touch the HTML directly, so they override CSS rules.

##Patterns We've Noticed
**!important** trumps inline styles

###Power combos
**id** + **class** -----> id overrides
**element** 

ˇ
