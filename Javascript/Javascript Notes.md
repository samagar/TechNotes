## JavaScript Basics Notes
---
** SOURCE ** 
https://htmlcheatsheet.com/js/

### Basics
```
** On page script **
<script type="text/javascript"> ...</script> tion

** Include external JS file **optional
<script src="filename.js"></script> 

** Functions **
function addNumbers(a, b) 
{ return a + b; ;
}
x = addNumbers(1, 2);

** Edit DOM element **
document.getElementById("elementID").innerHTML = "He"

** Output **
console.log(a);         // write to the browser
document.write(a);      // write to the HTML
alert(a);               // output in an alert box
confirm("Really?");     // yes/no dialog, return
prompt("Your age?","0");    // input dialog. 

** Comments **
/* Multi line
comment */
// One line
```

### Data Types
```
var age = 18;                               // number ot declared
var name = "Jane";                          // string
var name = {first:"Jane", last:"Doe"};      // object
var truth = false;                          // boolean
var sheets = ["HTML","CSS","JS"];           // array
var a; typeof a;                            // undefined
var a = null;                               // value null

** Objects **
var student = { 
firstName:"Jane",               // object name
lastName:"Doe",                 // list of properties
age:18,
height:170,
fullName : function() {         // object function
    return this.firstName + " " + this.lastName; 
}
};
student.age = 19;               // setting value 
student[age]++;                 // incrementing
name = student.fullName();      // call object function
```

### Variables
```
var a;                          // variable
var b = "init";                 // string
var c = "Hi" + " " + "Joe";     // "Hi Joe"
var d = 1 + 2 + "3";            // "33"
var e = [2,3,5,8];              // array
var f = false;                  // boolean
var g = /()/;                   // RegEx
var h = function(){};           // function object
const PI = 3.14;                // constant
var a = 1, b = 2, c = a + b;    // Variables on one line
let z = 'zzz';                  // block scope local variable

** Strict Mode **
"use strict";   // Use strict mode to write secure code
x = 1;  // Throws an error because variable is not declared Values

** values **
false, true                     // boolean
18, 3.14, 0b10011, 0xF6, NaN    // number
"flower", 'John'                // string
undefined, null , Infinity      // special
```

### Operators
```
a = b + c - d;      // addition, substraction
a = b * (c / d);    // multiplication, division
x = 100 % 48;       // modulo. 100 / 48 remainder = 4
a++; b--;           // postfix increment and decrement

** Bitwise operators **
&	AND 	        5 & 1 (0101 & 0001)	1 (1)
|	OR 	            5 | 1 (0101 | 0001)	5 (101)
~	NOT 	        ~ 5 (~0101)	10 (1010)
^	XOR 	        5 ^ 1 (0101 ^ 0001)	4 (100)
<<	left shift 	    5 << 1 (0101 << 1)	10 (1010)
>>	right shift 	5 >> 1 (0101 >> 1)	2 (10)
>>>	zero fill right shift 	 5 >>> 1 (0101 >>> 1)	2 (10)

** Arithmetic **
a * (b + c)         // grouping
person.age          // member
person[age]         // member
!(a == b)           // logical not
a != b              // not equal
typeof a            // type (number, object, function...)
x << 2  x >> 3      // minary shifting
a = b               // assignment
a == b              // equals
a != b              // unequal
a === b             // strict equal
a !== b             // strict unequal
a < b   a > b       // less and greater than
a <= b  a >= b      // less or equal, greater or eq
a += b              // a = a + b (works with - * %...)
a && b              // logical and
a || b              // logical or
```

### Loops
```
** For Loop **
for (var i = 0; i < 10; i++) { 
document.write(i + ": " + i*3 + "<br />"); 
}

var sum = 0;
for (var i = 0; i < a.length; i++) {
sum + = a[i];
} 

// parsing an array
html = "";
for (var i of custOrder) {
html += "<li>" + i + "</li>";
}

** While Loop **
var i = 1;              // initialize
while (i < 100) {       // enters the cycle
i *= 2;                 // increment to avoid in
document.write(i + ", "); // output
}

** Do While Loop **
var i = 1;          // initialize
do {                // enters cycle at l
i *= 2;             // increment to avoid
document.write(i + ", "); // output
} while (i < 100)           // repeats cycle

** Break **
for (var i = 0; i < 10; i++) {
if (i == 5) { break; } // stops and exits 
document.write(i + ", "); // last output number 
}

** Continue **
for (var i = 0; i < 10; i++) {
if (i == 5) { continue; } // skips the rest 
document.write(i + ", "); // skips 5
}
```
** If else ** 
if ((age >= 14) && (age < 19)) { 
status = "Eligible.";
} else {
status = "Not eligible.";
}

** switch ** 
switch (new Date().getDay()) { 
case 6:
        text = "Saturday"; 
        break;
case 0:
        text = "Sunday"; break;        
default:
        text = "Whatever";
}

### Errors
```
try { 
undefinedFunction();
}
catch(err) { 
console.log(err.message); 
}

** Throw error **
throw "My error message"; 

** Input validation **
var x = document.getElementById("mynum").value; 
try {
if(x == "") throw "empty"; 
if(isNaN(x)) throw "not a number"; 
x = Number(x);
if(x > 10) throw "too high";
}
catch(err) { 
document.write("Input is " + err); 
console.error(err);
}
finally {
document.write("</br />Done");
}

** Error name values **
RangeError ReferenceError SyntaxError TypeError URIError
```

### Strings
```
var abc = "abcdefghijklmnopqrstuvwxyz";
var esc = 'I don\'t \n know';       // \n new line
var len = abc.length;       // string length
abc.indexOf("lmno");        // find substring
abc.lastIndexOf("lmno");    // last occurence
abc.slice(3, 6);            // cuts out "def"
abc.replace("abc","123");   // find and replace,
abc.toUpperCase(); 
abc.toLowerCase(); 
abc.concat(" ", str2);  // abc + " " + str2
abc.charAt(2);  // char at index
abc[2]; 
abc.charCodeAt(2); 
abc.split(","); 
abc.split(""); 
128.toString(16);   // number to hex(16)
```

### Arrays
```
var dogs = ["Bulldog", "Beagle", "Labrador"];
var dogs = new Array("Bulldog", "Beagle", "Labrador");

alert(dogs[1]);                 // access value at index 
dogs[0] = "Bull Terier";        // change the first item

for (var i = 0; i < dogs.length; i++) { 
console.log(dogs[i]);
}

** Methods **
dogs.toString();
dogs.join(" * ");
dogs.pop(); 
dogs.push("Chihuahua"); 
dogs[dogs.length] = "Chihuahua"; 
dogs.shift(); 
dogs.unshift("Chihuahua"); 
delete dogs[0];
dogs.splice(2, 0, "Pug", "Boxer");
var animals = dogs.concat(cats,birds); // join two
dogs.slice(1,4);
dogs.sort();
dogs.reverse();
x.sort(function(a, b){return a - b}); x.sort(function(a, b){return b - a});
highest = x[0];
x.sort(function(a, b){return 0.5 - Math.random()});

** additional functions **
concat, copyWithin, every, fill, filter, find, findIndex, forEach, indexOf, isArray, join, lastIndexOf, map, pop, push, reduce, reduceRight, reverse, shift, slice, some, sort, splice, toString, unshift, valueOf
```

### Numbers & Math
```
var pi = 3.141;
pi.toFixed(0);          // returns 3
pi.toFixed(2);          // returns 3.14 - for working with money
pi.toPrecision(2)       // returns 3.1
pi.valueOf();           // returns number
Number(true);           // converts to number
Number(new Date())      // number of milliseconds since 1970
parseInt("3 months");   // returns the first number: 3
parseFloat("3.5 days"); // returns 3.5
Number.MAX_VALUE        // largest possible JS number
Number.MIN_VALUE        // smallest possible JS number
Number.NEGATIVE_INFINITY// -Infinity
Number.POSITIVE_INFINITY// Infinity

** Math.**
var pi = Math.PI;       // 3.141592653589793
Math.round(4.4);        // = 4 - rounded
Math.round(4.5);        // = 5
Math.pow(2,8);          // = 256 - 2 to the power of 8
Math.sqrt(49);          // = 7 - square root 
Math.abs(-3.14);        // = 3.14 - absolute, positive value
Math.ceil(3.14);        // = 4 - rounded up
Math.floor(3.99);       // = 3 - rounded down
Math.sin(0);            // = 0 - sine
Math.cos(Math.PI);      // OTHERS: tan,atan,asin,acos,
Math.min(0, 3, -2, 2);  // = -2 - the lowest value
Math.max(0, 3, -2, 2);  // = 3 - the highest value
Math.log(1);            // = 0 natural logarithm 
Math.exp(1);            // = 2.7182pow(E,x)
Math.random();          // random number between 0 and 1
Math.floor(Math.random() * 5) + 1;  // random integer, from 1 to 5

** Constants like Math.PI:**
E, PI, SQRT2, SQRT1_2, LN2, LN10, LOG2E, Log10E
```

### Regex - Regular Expressions 
```
var a = str.search(/CheatSheet/i);

** Modifiers **
i perform case-insensitive matching
g perform a global match
m perform multiline matching

** Patterns **
\       Escape character
\d      find a digit
\s      find a whitespace character
\b      find match at beginning or end of a word
n+      contains at least one n
n*      contains zero or more occurrences of n
n?      contains zero or one occurrences of n
^       Start of string
$       End of string
\uxxxx  find the Unicode character
.       Any single character
(a|b)   a or b
(...)   Group section
[abc]   In range (a, b or c)
[0-9]   any of the digits between the brackets
[^abc]  Not in range
\s      White space
a?      Zero or one of a
a*      Zero or more of a
a*?     Zero or more, ungreedy
a+      One or more of a
a+?     One or more, ungreedy
a{2}    Exactly 2 of a
a{2,}   2 or more of a
a{,5}   Up to 5 of a
a{2,5}  2 to 5 of a
a{2,5}? 2 to 5 of a, ungreedy
[:punct:]   Any punctu­ation symbol
[:space:]   Any space character
[:blank:]   Space or tab

```

### Events
```
<button onclick="myFunction();">
Click here
</button>

** Mouse **
onclick, oncontextmenu, ondblclick, onmousedown, onmouseenter, onmouseleave, onmousemove, onmouseover, onmouseout, onmouseup

** Keyboard **
onkeydown, onkeypress, onkeyup

** Frame ** 
onabort, onbeforeunload, onerror, onhashchange, onload, onpageshow, onpagehide, onresize, onscroll, onunload

** Form **
onblur, onchange, onfocus, onfocusin, onfocusout, oninput, oninvalid, onreset, onsearch, onselect, onsubmit

** Drag **
ondrag, ondragend, ondragenter, ondragleave, ondragover, ondragstart, ondrop

** Clipboard **
oncopy, oncut, onpaste

** Media **
onabort, oncanplay, oncanplaythrough, ondurationchange, onended, onerror, onloadeddata, onloadedmetadata, onloadstart, onpause, onplay, onplaying, onprogress, onratechange, onseeked, onseeking, onstalled, onsuspend, ontimeupdate, onvolumechange, onwaiting

** Animation ** 
animationend, animationiteration, animationstart

** Miscellaneous **
transitionend, onmessage, onmousewheel, ononline, onoffline, onpopstate, onshow, onstorage, ontoggle, onwheel, ontouchcancel, ontouchend, ontouchmove, ontouchstart

```

### JSON
```
var str = '{"names":[' +                        // crate JSON object
'{"first":"Hakuna","lastN":"Matata" },' +
'{"first":"Jane","lastN":"Doe" },' +
'{"first":"Air","last":"Jordan" }]}';

obj = JSON.parse(str);                      // parse
document.write(obj.names[1].first);         // access

** Send **
var myObj = { "name":"Jane", "age":18, "city":"Chicago" };  // create object
var myJSON = JSON.stringify(myObj);                         // stringify
window.location = "demo.php?x=" + myJSON;                   // send to php

** Storing and retrieving **
myObj = { "name":"Jane", "age":18, "city":"Chicago" };
myJSON = JSON.stringify(myObj);                // storing data

localStorage.setItem("testJSON", myJSON);   
text = localStorage.getItem("testJSON");       // retrieving data 

obj = JSON.parse(text);
document.write(obj.name);
```

### Promise
```
function sum (a, b) {
return Promise(function (resolve, reject) { 
 setTimeout(function () {                                // send the response after 1 second
  if (typeof a !== "number" || typeof b !== "number") {     // testing input types
	return reject(new TypeError("Inputs must be numbers"));
  }
  resolve(a + b);
 }, 1000);
});
}

var myPromise = sum(10, 5);
myPromsise.then(function (result) {
document.write(" 10 + 5: ", result);
return sum(null, "foo");              // Invalid data and return another promise
}).then(function () {                   // Won't be called because of the error
}).catch(function (err) {               // The catch handler is called instead, after another second
console.error(err);                   // => Please provide two numbers to sum.
});

** States **
pending, fulfilled, rejected

** Properties **
Promise.length, Promise.prototype

** Methods **
Promise.all(iterable), Promise.race(iterable), Promise.reject(reason), Promise.resolve(value)
```
