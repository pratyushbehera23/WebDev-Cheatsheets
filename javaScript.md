# JS

JavaScript abbreviated as JS is a high level Object Oriented Progamming language.
This language used in development of frontEnd as well as in the backEnd of website.

- JavaScript works like the brain of a website.
- There are so many libraries of JavaScript which makes the code shorter like jQuery and some frameworks of javascript that help building web-apps faster like ReactJs, AnuglarJs, VueJs.
- Javascript is one of the Languages which is compalsury to learn for a Web-Developers.

JavaScript is used in all popular browsers and standardized by ECMA as EcmaScript versions.
ECMA - org that defines standards
ECMAscript - specification  ex: ES6
JavaScript - lang that confirms to this specification

Using JS we can build: WebApp Games Command-line-tools Real-time-networking like chats

JS was created only for browsers, to work inside browser engines like: Chrome v8, Firefox spidermonkey, etc.
Later, found a way to run it outside browsers like in PC and servers. ex: Node, Deno, etc.
Node = (v8 engine) + (C++ program) - it makes JS run outside browser.
So, JS can be run inside a browser or in Node as they provide a runtime environment for JS code.

## Basis

### Variables

var let const

```js
var myname = "Pratyush";
var myname = "Chase";
myname = "Eli";

var no = 23;

let a = 5;
// let a = 3; ERROR as let is a block variable; it can be Initialize once
a = 3; //this is the right way to change value of let

const value = 55;   //the value of the const variable can't be changed
```

### Data types

Integer Boolean String

```js
let string = "Myself Pratyush";
let Num = 55;
let Number = 55.55;
let Bool = true;
let Boolean = false;
let Array = ['string',55,true]
let Object = { 
    name : 'pratyush' ,
    age : 19 ,
    hobby : 'programming'
    }
var undefined;
var ud = undefined;
let values = Null;

typeof(Num);
```

### Operators

- Arithmetic Operators:
  - Addition (+)
  - Subtraction (-)
  - Multiplication (*)
  - Division (/)
  - Exponention/power (**)
% Modulus(power)
++ Increment
-- Decrement

- Assignment Operators: =  +=  -=  *=  /=  %= **=

Comparison Operators:
== Equal to
=== Equal value and Equal data type
!= Not equal
!== Not equal value or not equal data type
> Greater than
< Lesser than
>= Greater than or equal to
<= Less than or equal to

Logical Operators:
&&  Logical and
||  Logical or
!   Logical Not

### Keywords

abstract arguments boolean break
byte case catch char
const continue debugger default
delete do double else
eval false final finally
float for function goto
if implements in instanceof
int interface let long
native new null package
private protected public return
short static switch synchronized
this throw throws transient
true try typeof var
void volatile while with

## Code

```js
// O/P:
console.log();
// ALERT box
alert("sometext");
// CONFIRM box
confirm("sometext");
// PROMPT box
prompt("sometext");
// Implementing HTML Tags in JS
document.write("<h1>Hello World</h1>");

// CONDITIONAL statements

// if  else  else if
if(55 == 55){
    document.write("55 is really equals to 55");
    }

if(55 == 54){
    document.write("55 is really equals to 54");
    }else{
    document.write("Condition is wrong");
    }

if(55 == 54){
    document.write("55 is really equals to 54");
    }else if(55 == 55){
    document.write("Condition is true");
    }else{
    document.write("Condition is wrong");
    }

// Switch case
switch(55) {
    case 54:
        document.write("55 == 54")
        break;
    case y:
        document.write("55 == 55");
        break;
    default:
        document.write("all conditions are wrong");
}

// Conditional Ternary
(55 == 54) ? document.write("condition is true") : document.write("condition is false");

// LOOP 

// while
let x = 1;
while(x > 10){
    document.write("The value is " + x);
    x++;
}

// do while
let y = 1;
do {
    document.write("The value is " + y);
    y++;
}while(y > 10)

// for
// for(var z=1, z>10, z++){
//     document.write("The value is " + z);
//     z++;
// }
/*
    for(let x = 1,x > 10,x++){
        document.write(“The value is “ + x);
        x++;
    }
*/

// for-of
let arrayy = ['vedansh','rohan','vanshika'];
    for(let valu of arrayy){
        document.write("The value is " + valu);
    }

// for-in
let obj = {
    First_Person : 'vedansh',
    Seconf_Person : 'rohan',
    Third_Person : 'vanshika'
    };
for(let key in obj){
    document.write("The value is " + obj[key]);
    }

// forEach
let arr = ['vedansh','rohan','vanshika'];
arr.forEach( (element,index) => {
    // document.write("The value is " + element + "and index is ” + index);
})

// FUNCTIONS
function Name(parameter){
    // code to be extecuted
    return value;
}

```

```js

var a,b,c;
a = parseInt(prompt("Enter a : "));
b = parseInt(prompt("Enter b : "));
c = a + b;
document.write(c);
```

```js
// JS

// print
console.log("Hello");

// variable
var myName = 'Pratyush';
console.log(myName);

let num = 23;
console.log(num);

// array
var items = ['Macbook', 'Guitar', 'Books', 'Music', 'Jaguar'];
var imp = items[4];

// conditional
var color = 'blue';
if (color === 'blue'){
    console.log("It's blue");
}

var bananas = 'yellow';
var numberBananas = 8;
if (bananas !== 'green'){
    if (numberBananas > 5){
        console.log("Let's make banana shake");
    }
}

// math arithmetic  + - * /
var x = 5;
x = x + 8;
console.log('x is ' + x);
x = x - 4;
console.log('x is now ' + x);

// 
if (x > 3 && x < 10){
    print('x is greater than 3 and smaller than 10')
}
if (x > 3 || x < 10){
    print('x is greater than 3 or smaller than 10')
}

// Loop
// For
for (var letter of 'hello'){
    console.log(letter);
}

var groceries = ['apples', 'milk', 'corn'];
for (var element of groceries){
    console.log(element);
}

for (var i = 0; i < 10; i = i + 1){
    console.log(i);
}

// Nestted loop

for (var state of ['Odisha', 'Goa', 'Andaman']) {
    for (var places of ['Summer', 'Beach', 'Tour']) {
        console.log('The' + state + ' ' + places)
    }
}

for (var state of [
    'Odisha',
    'Goa',
    'Andaman'
]) {
    for (var places of [
        'Summer',
        'Beach',
        'Tour'
    ]) {
        console.log('The' + state + ' ' + places)
    }
}

// 
var my_name = {
    first: 'Pratyush',
    last: 'Behera'
};
console.log(my_name.first + my_name.last);


// 
var myBackpack = {
    food: [
        'bananas',
        'nuts',
        'energy bar'
    ],
    equipment: [
        'map',
        'compass'
    ],
    clothing: [
        'jacket',
        'scarf',
        'hat'
    ]
}
console.log(myBackpack.food)
console.log(myBackpack.equipment)
console.log(myBackpack.clothing)

for (var element of myBackpack.equipment){
    if (element === 'map'){
        console.log("Map found");
    } else{
        console.log("Map not found")
    }
}

// 
var message = "Hello, this is Eli Shane!"
if (message.length > 30){
    console.log('It is ok');
} else{
    console.log('It is not ok');
}

// 

```
