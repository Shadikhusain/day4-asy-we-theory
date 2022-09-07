Q.1. what is the difference between Props and State?

Ans:Finally, let’s recap and see the main differences between props and state:

Components receive data from outside with props, whereas they can create and manage their own data with state
Props are used to pass data, whereas state is for managing data
Data from props is read-only, and cannot be modified by a component that is receiving it from outside
State data can be modified by its own component, but is private (cannot be accessed from outside)
Props can only be passed from parent component to child (unidirectional flow)
Modifying state should happen with the setState ( ) method
React.js is one today's of the most widely used JavaScript libraries that every front-end developer should know.

Q.2.Explain the useState API? explore

Ans:The state of your application is bound to change at some point. This could be the value of a variable, an object, or whatever type of data exists in your component.To make it possible to have the changes reflected in the DOM, we have to use a React hook called useState. It looks like this:

Q.3.Explain the how map, filter, reduce work.

Map:- The map() method is used for creating a new array from an existing one, applying a function to each one of the elements of the first array.

Syntax:
var new_array = arr.map(function callback(element, index, array) {
    // Return value for new_array
}[, thisArg])
In the callback, only the array element is required. Usually some action is performed on the value and then a new value is returned.

Example
In the following example, each number in an array is doubled.

const numbers = [1, 2, 3, 4];
const doubled = numbers.map(item => item * 2);
console.log(doubled); // [2, 4, 6, 8]

Filter:-
The filter() method takes each element in an array and it applies a conditional statement against it. If this conditional returns true, the element gets pushed to the output array. If the condition returns false, the element does not get pushed to the output array.

Syntax:
var new_array = arr.filter(function callback(element, index, array) {
    // Return true or false
}[, thisArg])
The syntax for filter is similar to map, except the callback function should return true to keep the element, or false otherwise. In the callback, only the element is required.

Examples:
In the following example, odd numbers are "filtered" out, leaving only even numbers.

const numbers = [1, 2, 3, 4];
const evens = numbers.filter(item => item % 2 === 0);
console.log(evens); // [2, 4]
In the next example, filter() is used to get all the students whose grades are greater than or equal to 90.

const students = [
  { name: 'Quincy', grade: 96 },
  { name: 'Jason', grade: 84 },
  { name: 'Alexis', grade: 100 },
  { name: 'Sam', grade: 65 },
  { name: 'Katie', grade: 90 }
];

const studentGrades = students.filter(student => student.grade >= 90);
return studentGrades; // [ { name: 'Quincy', grade: 96 }, { name: 'Alexis', grade: 100 }, { 


Reduce:-
The reduce() method reduces an array of values down to just one value. To get the output value, it runs a reducer function on each element of the array.

Syntax:
arr.reduce(callback[, initialValue])
The callback argument is a function that will be called once for every item in the array. This function takes four arguments, but often only the first two are used.

accumulator - the returned value of the previous iteration
currentValue - the current item in the array
index - the index of the current item
array - the original array on which reduce was called
The initialValue argument is optional. If provided, it will be used as the initial accumulator value in the first call to the callback function.
Examples
The following example adds every number together in an array of numbers.

const numbers = [1, 2, 3, 4];
const sum = numbers.reduce(function (result, item) {
  return result + item;
}, 0);
console.log(sum); // 10
In the next example, reduce() is used to transform an array of strings into a single object that shows how many times each string appears in the array. Notice this call to reduce passes an empty object {} as the initialValue parameter. This will be used as the initial value of the accumulator (the first argument) passed to the callback function.

var pets = ['dog', 'chicken', 'cat', 'dog', 'chicken', 'chicken', 'rabbit'];

var petCounts = pets.reduce(function(obj, pet){
    if (!obj[pet]) {
        obj[pet] = 1;
    } else {
        obj[pet]++;
    }
    return obj;
}, {});

console.log(petCounts); 


Q.4.Create your own map, filter, reducer methods and attach it to an array using prototype chain ( Unit 3 / JS-201 concept ).

map:-The map() method creates a new array with the results of calling a provided function on every element in the calling array.
Seems pretty straightforward. Now let’s see the Javascript map() in action!

const array1 = [1, 4, 9, 16];

// pass a function to map
const map1 = array1.map(x => x * 2);

console.log(map1);
// expected output: Array [2, 8, 18, 32]

filter:-The filter() method creates a new array with all elements that pass the test implemented by the provided function.

const words = ['spray', 'limit', 'elite', 'exuberant', 'destruction', 'present'];

const result = words.filter(word => word.length > 6);

console.log(result);
// expected output: Array ["exuberant", "destruction", "present"]

reduce:-The reduce() method executes a reducer function (that you provide) on each member of the array resulting in a single output value.

const array1 = [1, 2, 3, 4];

// 0 + 1 + 2 + 3 + 4
const initialValue = 0;
const sumWithInitial = array1.reduce(
  (previousValue, currentValue) => previousValue + currentValue,
  initialValue
);

console.log(sumWithInitial);
// expected output: 10








