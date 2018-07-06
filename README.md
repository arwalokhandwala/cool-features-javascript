# cool-features-javascript
This repository includes all new useful ES6, ES7 and ES8 features

# ECMAScript 6
 
### Why ES6 in the first place? Wasn't ES5 enough? 

* ES6 language design is clearer than ES5
* ES6 reduces boilerplate code Ex: `function VS arrow syntax`

### Cool..Lets get started !!!

- [block scope](#block-scope)
- [arrow function](#arrow-function)
- [template literals](#template-literals)
- [property shorthand](#property-shorthand)
- [object literals](#object-literals)
- [object destructuring](#object-destructuring)
- [default argument values](#default-argument-values)
- [startsWith, endsWith](#startswith-endswith)
- [includes](#includes)
- [padStart, padEnd](#padstart-padend)

### Block scope

Before ES6 JS had no way to support block level scope. Now we have.

* **var** which defines function level scope
* **let** which defines Block level scope

```Javascript 
var a = 20 

if(a > 10) {
  let b = 1
  let a = 2
  console.log(b,a, 'Inner Scope')   // 1 2 Inner Scope
}

console.log(a, 'Outer Scope')   // 20 Outer Scope
```
### Arrow function

Putting fun around functions :wink:

Before
```Javascript
function sayHello() {
  return 'Hello Guys!!'
}
```
After
```Javascript
let sayHello = () => 'Hello Guys!!'
```
### Template literals

Use **back tick(`)** instead of single quote or double quote

#### Multi Line Strings

Before
```Javascript
console.log('string text line 1\n' +
'string text line 2');
```
After
```Javascript
console.log(`string text line 1
string text line 2`);
```
#### Expression Interpolation

Before
```Javascript
var a = 5;
var b = 10;
console.log('The sum of a & b is ' + (a + b) + '.');
```
After
```Javascript
var a = 5, b = 10
console.log(`The sum of a & b is ${a + b}`)
```
### Property Shorthand

Before
```Javascript
var name = 'Arwa Lokhandwala';
var obj = {
  name: name,
}
console.log(obj)
```
After
```Javascript
var name = 'Arwa Lokhandwala'
var obj = {
  name
}
console.log(obj)
```
### Object Literals

#### Shorthand for writing Methods

Before
```Javascript
var obj = {
  add : function(a,b) {
    return a+b
  }
}
```

After
```Javascript
var obj = {
  add(a,b) {
    return a+b
  }
}
```
#### Computed Properties

Example
```Javascript
var i = 0
var fruits = {
  [`fruit ${++i}`] : 'Apple',
  [`fruit ${++i}`] : 'Mango'
} 
```
### Object Destructuring

Quickly extract values from objects and arrays

Example 1 (With Objects)
```Javascript
let animal = { type: 'dog', sound: 'woof', paws: 4 };
let {name, sound, paws} = animal;
console.log(sound, name); /// "woof undefined"
```
Example 2 (With Arrays)
```Javascript
let [n1, n2, n3, n4, ...r] = [100, 'three', 34, {number: 23}, 694, 'eighteen'];
console.log(n1, n2, n3, n4); // "100 'three' 34 { number: 23 }"
console.log(r); // "[ 694, 'eighteen' ]"
```
Example 3 (Nested Objects)
```Javascript
var details = {
  name: 'Arwa Lokhandwala',
  address: {
    areaName: 'Santacruz',
    pincode: '400055'
  }
}

let {address: {pincode: pincode}} = details
console.log(pincode) //400055
```
### Default Argument Values

Example
```Javascript
function greet(name = 'Anon', callback = function(){}) {
  console.log(`Hello ${name}!`);

  // No more "callback && callback()" (no conditional)
  callback();
}
```
### startsWith(), endsWith() 

**Only works with Strings**

Example
```Javascript
"MooTools".startsWith("Moo"); // true;
"MooTools".startsWith("moo"); // false;

"MooTools".endsWith("Tools"); // true;
```
### includes()

**Works with both Array and Strings** & **case-sensitive**

Example
```Javascript
'javascript'.includes('java')  // true

[1,2,3,4].includes(1) //true
```
### padStart(), padEnd()

padStart and padEnd allow us to pad a given string with any text of our choosing to ensure a string matches a given length

Example
```Javascript
'def'.padStart(6, 'abc') // 'abcdef'

'23'.padEnd(8, '0') // '23000000'
```
### Object Entries

Allows us to get an object's enumerable property pairs in array format.

Example
```Javascript
//Object
Object.entries({ 'a': 'A', 'b': 'B' }); // [["a","A"],["b","B"]]

// String
Object.entries('david') // [["0","d"],["1","a"],["2","v"],["3","i"],["4","d"]]
```
### Object Values

Provides only the values of an object

Example
```Javascript
Object.values({ 'a': 23, 'b': 19 }) // [23, 19]
```



