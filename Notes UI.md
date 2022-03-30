# Welcome to the CSD program.

## Stage 1
### HTML,CSS and Javascript
    Mandatory hands-on
    Additional hands-on
    Code Challenge - Timer based
### ANSI SQL using MySQL
    Mandatory hands-on
    Additional hands-on
    Code Challenge - Timer based
### Core Java (Java version 8)
    Mandatory hands-on
    Additional hands-on
    Code Challenge - Timer based

>KNOCK OUT CHALLENGE will be made active.

## Stage 2
    Maven 
    JUnit Testing 
    Spring Framework:Spring Core
    Spring MVC using Spring Boot
    Tekstac Platform


## Software Requirements
***
    * Notepad++
    * MySQL version 8
    * Java version 8
    * Eclipse IDE 2021-03
    * What is HTML?
    * Hypertext Markup Language is used for designing 
    * web pages to be rendered by the web browser, mobilebrowsers.

## HTML version 5
The first line we write is:
```Html
<!DOCTYPE html>
The line is used to tell the browser about the version of HTML
being used to design the web page.
We save an HTML page with .html extension
<html>
    <head></head>
    <body></body>
</html>
```


### There are two main types of tags we can write in HTML.
---
    a) content tags: <head></head>
    b) empty tags: <br/>,>hr/>
What is present in the `<head>` section of HTML?
    We add a `<title>` and `<meta>` as well as
    `<script>` and `<style>` tags to link external js and css file
    respectively.


## Meta : Data about Data
---
This viewport is the visible area of your screen on the browser.

```Html
<meta name="viewport" content="width=device-width,initial-scale=1.0"> 
```

In the `<meta>` tag you mention the author name, keywords,charset etc 
which is used by the search engines.
To redirect your web page to some other page after some time.

```html
<meta http-equiv="refresh" content="5;url=https://www.w3schools.com"/>
<link rel="stylesheet" href="style.css"/>
<link rel="icon" href="smiley.jpg"/>
```
CSS or Cascading Stylesheet is used to enhance the design of 
the web page.


`<!-- HTML Comment -->`

What is present in the `<body>` section of HTML?

All the visible content has to be added in the `<body>`
section

    a) Basic HTML tags
    b) Tags for <table>,lists <ol>,<ul>,<dl>,image <img>,
        hyperlinks <a href="{target}"/> etc
    c) Designing HTML form using <form> tag
    HTML entities: &lt; &gt; &amp; &quot; &copy;

```html
<!-- HTML Form -->
<form action="https://www.google.com">
<label for="abc">First Name:</label>
<input type="text" name="fname" id="abc"/><br/>
<label for="xyz">Last Name:</label>
<input type="text" name="lname" id="xyz"/><br/>
<input type="submit"/>
</form>

```
>On submit, the same page gets reloaded if no action attribute 
is mentioned.

The url is updated with a query string..
    
    C:/Users/HP/Desktop/BatchesNow/CSD/page2.html?fullname=Aman

The value of the name attribute will be used to capture the
response when the page is submitted on the server side.

    file:///C:/Users/HP/Desktop/BatchesNow/CSD/page2.html?fname=Vamsi&lname=Krishna
>The id attribute is used by the CSS and JavaScript for some 
processing.

>If not mentioned, the default way of sending data to the server
is through HTTP GET method.

This method is not secure even though it is faster as the info
is being passed through request header as a query string.
We can also use HTTP POST method `<form method="post"></form>`.

>The POST method is more secure but less fast.
 The information is passed through the request body.

## HTML 5 input attributes, we have explored
---

    a) required
    b) placeholder
    c) max, min
    d) maxlength,minlength
    e) pattern
    f) multiple (file)
    g) autocomplete
    h) autofocus="true"
    i) readonly (you cannot make any change but the
    info will be sent on the server side)
    j) disabled (will not be send on the server side)

## CSS (Cascading Style Sheet)
---
We can add CSS to HTML as
    
a) inline

    <img src="mickey.jpg" style="width:80px;height:80px;"/>
b) internal

    <style>
    div{
        background-color:pink;
        color:blue;
        border:2px solid black;
        border-radius:15px;        
    }
    </style>

c) external
    
    <link rel="stylesheet" href="style.css"/>
>inline >> internal >> external

### What are the different selectors we find in CSS?

a) universal selector

    *{
    color:rgb(60,150,220);
    }

b) element selector

    body{
        background-color:cyan;
    }

c) class selector

    .mandate{
        color:red;
    }
In the HTML portion
`<span class="mandate">*</span>`

d) id selector

```css
/* id selector */
#cap{    
    color:blue;
    text-transform:uppercase;
    font-family:Comic Sans MS;
    font-size:35px;
}
```    
In the HTML portion
```html
<caption id="cap">Registration Form</caption>
```
There are different styling rules given in the format
of key : value pairs

```css
    {
        color:blue;
        text-transform:uppercase;
        text-decoration:overline;
        font-family:Comic Sans MS;
        font-size:35px;
        font-weight:bold;

        background-color:red;
        background-image:url('mickey.jpg');
        background-repeat:repeat-y;
        border:2px solid black;
        border-radius:15px;
    }
```

margin: the surrounding space between the inner
element (div) and the outer element (div).

## CSS box model
------------------
    content: image, text,....
    border: is the line surrounding the content
    padding: space surrounding the content till the border is the padding
    margin: space surrounding the border and the enclosing container. 

```css
{
    margin:10px;/*applicable from all sides*/
    margin:10px 20px 30px 15px;/*TRBL*/
    margin-bottom:15px;
}
```

# JavaScript

>Javascript is used to make the web page responsive, dynamic and 
interactive by nature.

 Using JS, we can:

    a) dynamically add or remove elements from the page
    b) modify the styling rules at run time
    c) perform computations
    d) perform validations

What is JS?

    It is a loosely typed scripting language.

JS does not have any so called data type.We define a variable using
var keyword. The data type of the variable depends on the type of data
currently being stored in the variable.

```javascript
var num=5; //number
var name='Abhi'; //string
var num=7.89; //number
var num=true; //boolean
```

Points:

    a) What are the data types we find? 
    number,boolean,object,null,undefined,string,function
    b) Using typeof operator, you can check the current data type of
    a variable.
    c) The "name" is actually a keyword like thing; hence always assumes to be a string.
    d) console.log(x);//to show the output on the browser console; used in development
    time.
    e) == (value checking), === (value & data type)


```html
<script>    
    var z=true;
    console.log(z);
    console.log(typeof z);
    console.log(typeof z);
    
    var x=78.89;
    console.log(x);
    console.log(typeof x);
    console.log(typeof 78.89);
    
    var y='Abhi';
    console.log(y);
    console.log(typeof y);
    console.log(typeof 'Abhi');

    //Normal for loop
     var colors=['orange','red','blue','green'];
     for(var i=0;i<colors.length;i++)
     console.log(colors[i]);
    
    //Advanced for loops
    for(var i in colors)//in-> index
    console.log(colors[i]);
    
    for(var i of colors)//of->value
    console.log(i);
    
    for(var i of colors){
        console.log(i);
        if(i === 'red')
        console.log('my favorite you know');
    }

    //some methods of arrays
    var colors=['orange','red','blue','green'];
    console.log(colors.push('pink'));//current length
    colors.sort();//sort in asc order
    console.log(colors);

    //Java script object and props
    var user={
        fName:'Rahul',
        lName:'Jain',
        printName:function(){
            return this.fName+' says hello';
        }
    }
    console.log(user.printName());

    //function expression
    var sum=function(a,b){
        return a+b;
    }
    console.log(sum(5,6));
    console.log(typeof sum);

    //arrow function    
        var sum=(a,b)=>a+b;    
        console.log(sum(7,5));
        var prod=(a,b)=>a*b;
        console.log(prod(5,6));
    </script>
```

What are the different of dialog boxes we find in JS?

    a) alert(): to display some message to user
    b) prompt(): to accept non boolean input from user
    c) confirm(): to accept boolean response from user
```html
<!-- dialogue box -->
<script>
    var uname=prompt('Name');
    if(uname!= null && uname.trim().length>0){
        alert('Hello '+uname);
    }else
        alert('Welcome guest');
    
</script>   

<script>
    var resp=confirm('Have you understood?');
    if(resp)
        alert('Lets proceed');
    else
        alert('Lets repeat');    
</script>
```

What is the use of isNaN() function?

```javascript
    var resp=prompt('Enter a number');

    if(isNaN(resp)) //is not a number
        alert('Its not a number');
    else
        alert('You entered '+resp);
```
How is Number() different from parseInt() function?

    parseInt() accepts input till it doesn't encounter a non
    numeric character like any alphabet or even a .(dot).
    parseInt() not okay for decimal values.
    Number() can be used to accept decimal values, even will work
    for exponenial values but any alphanumeric values will not work.
```js
var resp=prompt('Enter a number');
var num=parseInt(resp);
alert('You entered '+num);
```

### What is DOM?

Document Object Model. It is the programming interface for
HTML.The browser creates a document object when it renders 
a web page.

    a) document.getElementById()
    b) document.getElementsByName()
    c) document.getElementsByTagName()
    d) document.getElementsByClassName()
    e) document.querySelector()
    f) document.write()

Example#1:
```html
Name:<input type="text" id="uname"/><br/>
<input type="button" value="Click" onclick="f1()"/><br/>
<span id='result'></span>

<script>
    function f1(){
    var uname=document.getElementById('uname').value;
    if(uname!=null && uname.trim().length>0)
        document.getElementById('result').innerText='Hello '+uname;
    else
        document.getElementById('result').innerText='welcome guest';    
    }
</script>
```

### Exploring Javascript
HTML and JavaScript being used together.
The document object is responsible for making the HTML
elements aka nodes to be available to the javascript
functions.

## Ex #0
```html
<script>
    function f1(){
    var uname=document.getElementById('uname').value;
    if(uname!=null && uname.trim().length>0)
        document.getElementById('result').innerHTML='<b>Hello '+uname+'</b>';
    else
        document.getElementById('result').innerText='<b>welcome guest</b>';    
    }
</script>
```

When you have any HTML `<input>` elements, we use value property
to either fetch the value or set the value.
    `document.getElementById('txt1').value='HTML';`
>innerText: The web browser will render the content as it is.
If there is any HTML tag then also no special effect will be there.

>innerHTML: The web browser will render the HTML tags(if present)
in the content.

## Ex #1

```html
<script>
    function f1(){
        var paras=document.getElementsByTagName('p');
        for(var i=0;i<paras.length;i++){
            paras[i].style.textTransform='uppercase';
            paras[i].style.color='blue';
        }
    }
</script>
```

Using Javascript coding, we have modified even the 
styling rule.

    font-family |fontFamily
    background-color |backgroundColor

## Ex 2#

```html
<script>
    function f1(){
        var price=document.getElementById('txtPrice').value;
        var qty=document.getElementById('txtQty').value;
        
        document.getElementById('outp').innerText=(price*qty);
    }
</script>

<div style="border:2px solid red;">
    Enter Price: <input type="number" min="1" id="txtPrice"/><br/>
    Enter Qty: <input type="number" min="1" max="10" id="txtQty"/><br/>
    <input type="button" onclick="f1()" value="Click"/>
    <br/>
    Total: <output id='outp' for="txtPrice txtQty"></output>
</div>
```


## Ex 3#

```html
<script>
    function f1(){
        var bs=document.getElementsByName('browsers');
        var cnt=0;
        var arr=new Array();
        for(var i in bs){
            if(bs[i].checked){
                cnt++;
                arr.push(bs[i].value);
            }
        }
        document.getElementById('sp').innerText=(cnt);
        document.getElementById('pp').innerText=(arr.toString());
    }
</script> 
```

>For radio and checkbox, we use checked property.
For select, we use selected property

## Ex #4
onsubmit() is associated with `<form>` tag.

```html
<script>
    function f1(){
        var bs=document.getElementsByName('browsers');
        var cnt=0;
        const arr=new Array();
        //arr=new Array();
        for(var i in bs){
            if(bs[i].checked){
                cnt++;
                arr.push(bs[i].value);
            }
        }
        document.getElementById('sp').innerText=(cnt);
        document.getElementById('pp').innerText=(arr);
        return false;
    }
</script>

<form onsubmit="return f1()">
<input type="submit" value="Send" />
    <br/>
</form>
```

## Ex #5
Client side validation using Javascript

```html
<script>
    function f1(){
        var uname=document.getElementById('txtUname').value;
        var password=document.getElementById('txtPassword').value;
        if(uname==null||password==null||uname.trim().length<=2){
            document.getElementsByTagName('span')[0].innerText='Fields are blank';
            return false;
        }
        if(password!=='p1234'){
            document.getElementsByTagName('span')[0].innerText='Incorrect Password';
            return false;
        }
            
        return true;
    }
</script>    

<form action="https://www.google.com" onsubmit="return f1()">
    <fieldset style="width:450px">
    <legend>Login</legend>
    <span style='color:red'></span><br/>
    
    User Name:<input type="text" id="txtUname"/><br/>
    Password:<input type="password" id="txtPassword"/><br/>
    <input type='submit'/>
    </fieldset>
</form>
```

## Ex #6
Example of keyPress event...

```html
<script>
    function f2(evt){
        var key=evt.keyCode;
        if(!(key>=48  && key <=57))
            evt.preventDefault();
    }
</script>
<input type="text" id="txtUname" onkeypress="f2(event)"/>
```


>The `preventDefault()` method cancels the event if it is cancelable, meaning that the default action that belongs to the event will not occur.
For example, this can be useful when:
Clicking on a "Submit" button, prevent it from submitting a form
Clicking on a link, prevent the link from following the URL

## Ex 7#
`onload()` & `date` example

```html
<script>
function f3(){
    var dt=new Date().toISOString().substring(0,10);
    document.getElementById('dtJoining').setAttribute('max',dt);
}
</script>
Joining:<input type="date" id="dtJoining" />
```

## Javascript functions
---
    a) array related functions: toString,push,pop,join,...
    b) string related functions: substring,search,uppercase,trim,length,...
    c) date functions:toISOString(),new Date(),getDate(),getMonth(),...
    d) dialog boxes: aler, confirm,prompt
    e) how to change the styling rule through JS?
        style.textTransform='uppercase';
    f) explore the events like onsubmit, onclick, onload,onchange,
    onmouseenter,onmouseleave,...
    g) more and more examples


### Example of onchange event

```html
<script>
    function f4(){    
        var city=document.getElementsByName('city');
        for(var c=0;c<city.length;c++){    
                document.getElementById('sp').innerHTML=(city[c].value);            
        }
    }
</script>
City: <select name="city" onchange="f4()">
    <option value="kolkata">Kolkata</option>
    <option value="pune">Pune</option>
    <option value="hyderabad">Hyderabad</option>
    <option value="chennai">Chennai</option>
</select><br/>
City of Choice: <span id="sp"></span>
```

### testing push
