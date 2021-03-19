#   how to type variables 
```scss
$main:rgb(211, 31, 31);
body {}

.class1 {}

.main {
     background: $main;

}
```

# /* ########### hints ##############*/
# ** hint
* extands start with % not class . example to did`t render
# (%) means placeholder selector (.) means class like html class

```css
.cover{
background: red;
}

%cover{
background: red;

} 
```
# ** hint
 import files by (@import) 
 if you need did`t compile file start file name with _ line _file.scss


<h1 style="text-align: center"> function to include </h1>
// @mixin for prefixes  to use it with lots of classes 

<h1 style="text-align: center"> example </h1>

#  function 
```scss
@mixin FuncName($varName is the prefix){
-webkit-border-image: $varName;
-moz-border-image: $varName;
-o-border-image: $varName;
border-radius: $varName;

}


//before like this
.classNaMe{
-webkit-border-image: 10px;
-moz-border-image: 10px;
-o-border-image: 10px;
border-radius: 10px;

}

//after like this
.classNaMe{
@include FuncName(10px) // 10px for all border radius no time to type all :XD
}
```

<h1 style="text-align: center"> end of functions </h1>

#  if - else conditions 
```scss
$myVar : any thing ;
@if condition == $myVar {
// do some thing
} @else {
     //do some thing 
}
```

#  end of if - else conditions 


#  props 

example :
```scss
$prop1 : font;
$prop2 : size;

.body{
   font-size: 20px  // before 
   #{prop1}-#{prop2}: 20px   // after
}
```

#  end of props 


#  for loop 

 <h1 style="text-align: center"> normal  example : </h1>


 ```css
  /*css*/
.div1{ color : red;}
.div2{ color : red;}
.div3{ color : red;}
.div4{ color : red;}
.div5{ color : red;}
.div6{ color : red;}
.div7{ color : red;}
.div8{ color : red;}
.div9{ color : red;}
.div10{ color : red;}
/* html*/
 <div class="div1">test</div>
 <div class="div2">test</div>
 <div class="div3">test</div>
 <div class="div4">test</div>
 <div class="div5">test</div>
 <div class="div6">test</div>
 <div class="div7">test</div>
 <div class="div8">test</div>
 <div class="div9">test</div>
 <div class="div10">test</div>
```

# // how to type for loop
<h3 style="text-align: left color: blue"> fisrt  (start from 1 to end)</h3>


```scss
@for $i from 1 through 10 {
//do some thing
}
// 2nd  (start from 1 to before end ) if ends at 10 then this ends at 9 
@for $i from 1 to 10 {
//do some thing
}
```
#  hints (
// for example : 
 //styling
 ```scss
.div#{i}{ color : red;}  
// just one line :XD using props 

//html
 <div class="div1">test</div>
 <div class="div2">test</div>
 <div class="div3">test</div>
 <div class="div4">test</div>
 <div class="div5">test</div>
 <div class="div6">test</div>
 <div class="div7">test</div>
 <div class="div8">test</div>
 <div class="div9">test</div>
 <div class="div10">test</div>
```

#  end of for loop 

# @each start 

<h1 style="text-align: center"> first : single list</h1>
example: 

```scss
@each $var in $list {
     // do some thing
}
// another example 

 $list : banana apple orange;

 @each $myVar in $list {
.#{myVAr} {
     color : red ;
     background : url('images/#{myVar}.png')  //to loop images XD
} 
}
//html
 <div class="banana">Banana</div>
 <div class="apple">Apple</div>
 <div class="orange">Orange</div>

```
# 2nd multiple list

```scss
 $list : banana apple orange;
 @each $myVar , $color , $hover in 
 (banana , yellow ,white) // for banana ( name , color, hover )
 (apple , red ,white) // for banana ( name , color, hover )
 (orange , orange ,orange) // for banana ( name , color, hover )
 {
.#{myVAr} {
     color : $color ;
     background : url('images/#{myVar}.png')  //to loop images XD
&:hover{
color : $hover;
}
} 
}
```

#  3rd map (key : value ) like object
```scss
 $list : (
     banana : yellow,
     apple : red,
     orange : orange
 )
 @each $myKey , $myValue in $list {
.#{myKey} {
     color : $myValue ;
     background : url('images/#{myVar}.png')  //to loop images XD
} 
}
```

