# Sequent-Animation-CSS
##Using


 - Javascript
    * Require Jquery


###Include File
```HTML
 <script src="js/jquery-3.1.0.min.js"></script>
 <script src="js/sani_css.js"></script> 
 <script src="js/sani_init.js"></script> 
``` 
###Init Script
```Javascript
var anime1 = new animation("begin","end","500"); //Set Animation Class 
$(document).ready(function() {
    init_sani();
    play_sani();
});
``` 
####Animetion Class
 - Class name: animation()
 - Attribute
    - from:   Type: [String]
              * CSS Class name with no transition attribute begin position *
              Start CSS Class
    - to:   Type: [String]
            * CSS Class name with transition attribute end position *
            Element will transition CSS Class to this class
    - delay:   Type: [Int] (millisacound)
               Animation will active delay after previous sequent Element active
 - Syntax
    - var animation_obj = new animation([Begin CSS Class],[End CSS Class],[Delay]); 
 - Example
    - ```var anime1 = new animation("begin","end","500");```

###HTML
```HTML
<div class='ani_box sani first begin'  sani-data="scroll:0,after:null,from_class:begin,to_class:end,delay:500">
    test1
</div>
<div class='ani_box sani' id='second' sani-data="scroll:0,after:.first,animation:anime1">
    test2
</div>
<div class='ani_box sani' id='s3' sani-data="scroll:0,after:#second,from_class:begin-2,to_class:end-2,delay:100">
    test3
</div>
```


###Attribute
```TEXT
sani-data : Animation Properties

scroll :
  Type: [Int]
  Animation will active after page scroll position

after :
  Type: [String] / null
  * DOM Element "ID" or "Class name" *
  Animation will active after reference DOM element active
  
from_class :
  Type: [String]
  * CSS Class name with no transition attribute begin position *
  Start CSS Class

to_class :
  Type: [String]
  * CSS Class name with transition attribute end position *
  Element will transition CSS Class to this class
  
delay :
  Type: [Int] (millisacound)
  Animation will active delay after previous sequent Element active
```
###Demo:
[https://dev-orisma.github.io/Sequent-Animation-CSS/test.html](https://dev-orisma.github.io/Sequent-Animation-CSS/test.html "Title")