# Generator-functions-
 
function* nums() {
 console.log('starting'); // A
 yield 1; // B
 console.log('yielded 1'); // C
 yield 2; // D
 console.log('yielded 2'); // E
 yield 3; // F
 console.log('yielded 3'); // G
}
var generator = nums(); // Returns the iterator. No code in nums is executed
generator.next(); // Executes lines A,B returning { value: 1, done: false }
// console: "starting"
generator.next(); // Executes lines C,D returning { value: 2, done: false }
// console: "yielded 1"
generator.next(); // Executes lines E,F returning { value: 3, done: false }
// console: "yielded 2"
generator.next(); // Executes line G returning { value: undefined, done: true }
// console: "yielded 3"
