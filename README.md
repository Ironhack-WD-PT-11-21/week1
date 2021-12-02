# WEEK 1 | JS Basics 🤯

<br>

## Primitive data types

```javascript
const firstName = "Anna"; // string
const age = 35; // number (integer and float numbers)
const language = undefined; // undefined (default value of a declared variable with no assigned value)
const favoriteColor = null; // null (does not exist)
const isHuman = true; // boolean
```

## Truthy vs. Falsy

```javascript
// Truthy
Boolean("some string"); // true
Boolean(true); // true
Boolean(1); // true
Boolean(789.0003); // true
Boolean([]); // true
Boolean(["cat", "dog", "bird"]); // true
Boolean({}); // true
Boolean({ name: "John", age: 98 }); // true
Boolean(firstName); // true
Boolean(age); // true
Boolean(isHuman); // true

// falsy
Boolean(0); // False
Boolean(false); // False
Boolean(null); // False
Boolean(undefined); // False
Boolean(language); // False
Boolean(favoriteColor); // False
```

## Logic operators

- and: &&
- or: ||
- not: !

```javascript
// logic
4 < 5 && isHuman; // true

4 > 5 || isHuman; // true

firstName === "Anna" || !isHuman; // true

favoriteColor || language; // false (falsy)

language && isHuman; // false (falsy)

firstName && isHuman; // true

firstName && (!isHuman || age < 18); // false
```

## String manipulation

```javascript
let firstName = "Anna";

let greatings = `Hello ${firstName}! How are you doing?`;

console.log(greatings); // --> 'Hello Anna! How are you doing?'

greatings.length; // 30

greatings[2]; // ==> l

greatings.charAt(2); // ==> l

greatings.slice(6, 11); // --> Anna!

greatings.split(" "); // --> [ 'Hello', 'Anna!', 'How', 'are', 'you', 'doing?' ]
```

## Conditional

### if ... else

```javascript
if (firstName === "Anna") {
  greatings = "Hello again Anna !";
} else {
  greatings = `Welcome ${firstName} :)`;
}
```

### switch

```javascript
switch (age) {
  case 40:
    // do smth
    break;
  case 30:
    // do smth
    break;
  default:
  // do smth by default
}
```

## loops

### for loop

```javascript
for (let i = firstName.length - 1; i >= 0; i--) {
  console.log(firstName[i]);
}
```

### for ... of loop

```javascript
for (char of firstName) {
  console.log(char);
}
```

### while loop

```javascript
let counter = 0;

while (counter < 10) {
  counter += 1;
  console.log(counter);
}
```

### do ... while loop

```javascript
do {
  counter -= 1;
  console.log(counter);
} while (counter > 0);
```

## Arrays

```javascript
const pets = ["dog", "cat", "bird"];
pets[2]; // bird
pets[8764]; // undefined

pets.indexOf("cat");

pets.length;

const nestedArray = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9],
];
nestedArray[0]; // [1,2,3]

pets.push("mouse");
console.log(pets);

const lastPet = pets.pop();
console.log(lastPet);
console.log(pets);

const firstPet = pets.shift();
console.log(lastPet);
console.log(pets);

pets.unshift("dragon");
console.log(pets);

const secondAndThirdPets = pets.splice(1, 2);
console.log(secondAndThirdPets);
console.log(pets);
```

## ⚠️ .splice( ) vs. .slice( )

<br>

### .splice

```javascript
const numbers = [1, 2, 3, 4, 5, 6];

const splicedNumbers = numbers.splice(2, 3);

console.log(splicedNumbers); // [ 3, 4, 5 ]
console.log(numbers); // [ 1, 2, 6 ]
```

### .slice

```javascript
const slicedNumbers = numbers.slice(2, 3);

console.log(slicedNumbers); // [ 3 ]
console.log(numbers); // [ 1, 2, 3, 4, 5, 6 ]
```

## Functions

```javascript
function add(a, b) {
  // delaring a function
  const result = a + b;
  return result;
}

add(12, 7); // calling a function

const five = add(2, 3);
console.log(five);
```

<br>

```javascript
// forEach
function isOdd (number) {
  return number % 2 !== 0); // true or false
};

const numbersList = [1,2,3,4,5,6,7,8,9,10];
const oddNumbers = [];
const evenNumbers = [];


numbersList.forEach(function (number) {

  if( isOdd(number) ) {
    console.log(`${number} is an odd number`);
    oddNumbers.push(number);
  } else {
    console.log(`${number} is an even number`);
    evenNumbers.push(number);
  }
});


// map
function double (number) {
  return number * 2;
};

const doubleNumbers = numbersList.map(function (number) {
  return double(number);
});

console.log(doubleNumbers);
```

## Objects

```javascript
const person = {
  name: "Paul",
  age: 97,
  isHuman: true,
};

console.log(person);

person.name; // 'Paul'
person["name"]; // 'Paul'

let propertyIWant = "name";

person[propertyIWant]; // 'Paul'

Object.keys(person); // ['name', 'age', 'isHuman']
Object.values(person); // ['Paul', 97, true]

person.pets = ["cat", "rabbit"];
console.log(person);

delete person.isHuman;
console.log(person);

person.pets.push("dog");
console.log(person);

console.log("name" in person); // true

for (let key in person) {
  console.log(key);
}
```

# Git

```bash
$ git clone https......
$ git status
$ git add .
$ git commit -m "my first commit"
$ git push
```

# Command line

```bash
$ pwd
$ cd myFolder
$ cd ..
$ open <fileName>

$ npm run <script>
```

🌈
