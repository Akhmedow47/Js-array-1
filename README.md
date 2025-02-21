# JavaScript Destructuring, Spread, and Rest

## 1. Destructuring

### Array Destructuring
```javascript
let fruits = ['Apple', 'Banana', 'Orange'];
let [first, second] = fruits;
console.log(first);  // 'Apple'
console.log(second); // 'Banana'
You can skip elements: 
```
```
let [, secondFruit] = fruits;
console.log(secondFruit); // 'Banana'
Object Destructuring
let person = { name: 'John', age: 30 };
let { name, age } = person;
console.log(name); // 'John'
console.log(age);  // 30 
```
## You can also rename variables:

```
let { name: fullName, age: years } = person;
console.log(fullName); // 'John'
console.log(years);    // 30
```
## 2. Spread Operator

### Spread in Arrays
```
let fruits = ['Apple', 'Banana', 'Orange'];
let moreFruits = [...fruits, 'Mango', 'Peach'];
console.log(moreFruits);  // ['Apple', 'Banana', 'Orange', 'Mango', 'Peach']
```

## Spread in Objects
```
let person = { name: 'John', age: 30 };
let updatedPerson = { ...person, city: 'New York' };
console.log(updatedPerson); // { name: 'John', age: 30, city: 'New York' }
```
## 3. Rest Operator

```Rest in Function Parameters
function sum(...numbers) {
  return numbers.reduce((total, num) => total + num, 0);
}
console.log(sum(1, 2, 3, 4)); // 10
Rest in Array Destructuring
let fruits = ['Apple', 'Banana', 'Orange', 'Mango'];
let [firstFruit, secondFruit, ...restFruits] = fruits;
console.log(firstFruit);   // 'Apple'
console.log(secondFruit);  // 'Banana'
console.log(restFruits);   // ['Orange', 'Mango']
```
### Rest in Object Destructuring
```
let person = { name: 'John', age: 30, city: 'New York' };
let { name, ...otherDetails } = person;
console.log(name);         // 'John'
console.log(otherDetails); // { age: 30, city: 'New York' }
```
### Conclusion

*Destructuring allows you to unpack values from arrays and objects into variables.
Spread lets you copy and merge elements from arrays and objects.
Rest enables you to collect multiple elements into a single variable, useful in functions and destructuring.
These features make working with arrays and objects more concise and readable.*


