109775240991576903109775240991576903109775240991576903109775240991576903k109775240991576903109775240991576903# workbook
### Q1. Provide an overview and description of a standard source control process for a large project

A standard source control process consists of the following processes
- use a version control system such as git or svn, 
- establish a work flow that the team agrees with (like working on a feature branch or working on a clone)
- update source codes regularly and solve any merging conflicts 
- regularly commit the changes with well documentation about the changes you made
- and create a pull request before pushing to the source code


### Q2	What are the most important aspects of quality software?

- Maintainability - how modularized is the software and what is the effort to maintain and debug the source code
- testability - how does this software meet the objectives and how it is tested(auto tested ot manul tested)
- and usability - is it well documented and are there enough instructions to setup development environment

### Q3	Outline a standard high level structure for a MERN stack application and explain the components
![mern-architecture](https://user-images.githubusercontent.com/8579501/70398555-6ca69980-1a68-11ea-91fb-71fc7aa16486.png)

- Front-end development:   
  The front end componet responses to end user interactions and the 
  communication with server. In the structure displayed above, it uses React Js as its main framework which handles the user interactions and renders the information received from server.
- Back-end development:  
  The back end component responses to front end requests and database management. Express web framework is an open-source and light weighted web framwork for Node Js. And Mongoose is the main database for MERN development as other databases like SQL are not compatible with Node Js.
- Database management:  
  MongoDB is the native driver for interacting with a mongodb instance. In this example, it is used as the shell for Mongoose.

### Q4	A team is about to engage in a project, developing a website for a small business. What knowledge and skills would they need in order to develop the project?
- Version control:  
  - Effective use of version control software such as github or svn
  - Establish a working flow that the whole team agrees with such as working on new branchs or a clone copy
  - Effectively review pull request
- Automate testing
  - Use appropriate testing framwrok
  - Implement testing at early stage
  - Test whenever there is new change
- Project management
  - Effectively use project management tool such as trello or slack
  - Apply agile methodology
- Deployment
  - Deploy the project at early stage
  - Deploy the project to appropriate platform such as github or heroku
- Regular team meeting
  - daliy stand up
- Coding
  - Keep code dry
  - Write usful commit messages
  - Commenting on code

### Q5	With reference to one of your own projects, discuss what knowledge or skills were required to complete your project, and to overcome challenges

With reference to my rails project, I found following skills are useful:
- Deployment to cloud platform
- Effective version control such as frequent commits
- Implement testing
- Keep code dry and well documented
- Effective use of project management tool such as trell or slack
- Use an agile methodology

### Q6	With reference to one of your own projects, evaluate how effective your knowledge and skills were for this project, and suggest changes or improvements for future projects of a similar nature

With reference to my rails project, it is much easier to deploy the project at early stage than at later stage. As the deployed code may not work in cloud platform, so it could save more time in debuging. 

Another thing worths to do at early stage is the automated testing. From the last project experinece, I found it is frustrated and challenging when I tried to test all codes at later stage. Another benefit of doing this early is that it is eaier to check if there are any broken codes and less time to debug.

### Q7	Explain control flow, using an example from the JavaScript programming language
```javascript
const arr = ['a', 'b', 'c'];
for (let i=0; i<arr.length; i++) {
  console.log(arr[i]);
}

// Output:
// 'a'
// 'b'
// 'c'
```
The above piece of code is an example of loop workflow whcih loops through an arrary of 3 strings and print each element to console. 

### Q8	Explain type coercion, using examples from the JavaScript programming language

Each operation (function, operator, etc.) expects its parameters to have certain types. If a value doesn’t have the right type for a parameter, the two most common options for a caller are explicit convertion and implicit convertion.
```javascript
// explicit convertion:
Number('3') * Number('2')

// implicit convertion:
'3' * '2'
```
JavaScript initially didn’t have exceptions, which is why it uses coercion and error values for most of its operations:

```javascript
// Coercion
assert.equal(3 / true, 3);

// Error values
assert.equal(1 / 0, Infinity);
assert.equal(Number('xyz'), NaN);
```

### Q9	Explain data types, using examples from the JavaScript programming language

Javascript is both dynamically typed and weakly typed.

Dynamically typed languages infer variable types at runtime. This means once the code is run the compiler/interpreter will see your variable and its value then decide what type it is. The type is still enforced here, it just decides what the type is.

```javascript
var a = 1 // int
b = 'test' // string
```
Weakly typed languages allow types to be inferred as another type. For example, 1 + '2' // '12' In JS it sees the code is trying to add a number with a string — an invalid operation — so it coerces your number into a string and results in the string ‘12’.

```javascript
> 1+'12'
'12'
```

There are also 6 primitive types which is including:
- Boolean
- Null
- Undefined
- Number
- String
- Symbol

Everything else is an Object type.

### Q10	Explain how arrays can be manipulated in JavaScript, using examples from the JavaScript programming language

There are many native methods in JS that can manipulate array such as slice() that can grab a section of an array at once.

```javascript
var fruits = new Array ( "apple", "pear", "orange", "banana" );
alert ( fruits.slice ( 1, 3 ) )  // Displays "pear,orange"
alert ( fruits.slice ( 0, -2 ) ) // Displays "apple,pear"
alert ( fruits.slice ( 2 ) )     // Displays "orange,banana"
```
Other examples like push() will insert a new element at the end of array and pop() will get the first element of array and delete it afterwards.

```javascript
var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.push("Kiwi");       //  Adds a new element ("Kiwi") to fruits
```

```javascript
var fruits = ["Banana", "Orange", "Apple", "Mango"];
var x = fruits.pop();      // the value of x is "Mango"
```

### Q11	Explain how objects can be manipulated in JavaScript, using examples from the JavaScript programming language

We can use constructor to initialize the object JS. We can also define methods inside an object.
```javascript
function Person(first, last, age, eye) {
  this.firstName = first;
  this.lastName = last;
  this.age = age;
  this.eyeColor = eye;
}
```
Here is an example of adding an instance of object.
```javascript
var myFather = new Person("John", "Doe", 50, "blue");
var myMother = new Person("Sally", "Rally", 48, "green");
```
To add a new property to an object:
```javascript
myFather.nationality = "English";
```

### Q12	Explain how JSON can be manipulated in JavaScript, using examples from the JavaScript programming language

In javascript, JSON file is always in name/value pairs. And the JSON format is syntactically identical to the code for creating JavaScript objects.   
Because of this similarity, a JavaScript program can easily convert JSON data into native JavaScript objects.  
An example of JSON file:
```javascript
{
"employees":[
  {"firstName":"John", "lastName":"Doe"},
  {"firstName":"Anna", "lastName":"Smith"},
  {"firstName":"Peter", "lastName":"Jones"}
]
}
```
However, it will take too much memory to store data in object format. It can be done with JSON.stringify() which saves the data in text format, like this:
```javascript
var text = '{ "employees" : [' +
'{ "firstName":"John" , "lastName":"Doe" },' +
'{ "firstName":"Anna" , "lastName":"Smith" },' +
'{ "firstName":"Peter" , "lastName":"Jones" } ]}';
```
Then, use the JavaScript built-in function JSON.parse() to convert the string into a JavaScript object:
```javascript
var obj = JSON.parse(text);
```
### Q13	For the code snippet provided below, write comments for each line of code to explain its functionality. In your comments you must demonstrates your ability to recognise and identify functions, ranges and classes




```javascript
// define class
class Car {
  // initialize the car brand
  constructor(brand) {
    this.carname = brand;
  }
  // takes no argument and returns a string with car brand
  present() {
    return 'I have a ' + this.carname;
  }
}

// Model is a child class of Car class
class Model extends Car {
  // initialize the Model class with 2 parameters
  constructor(brand, mod) {
    // access the parent class
    super(brand);
    this.model = mod;
  }
  // takes no parameters and return a string
  show() {
    // call parent class function
    return this.present() + ', it was made in ' + this.model;
  }
}
// initilaize an array with elements of 4
let makes = ["Ford", "Holden", "Toyota"]
// Array.from loops through an array with length of 40 and creates a new array that stores the value that euqals to the index of each element plus 1980 (e.g 0+1980=1980, 1+1980=1981...39+1980=2019)
let models = Array.from(new Array(40), (x,i) => i + 1980)
// return a random number from a given range
function randomIntFromInterval(min,max) { // min and max included
    return Math.floor(Math.random()*(max-min+1)+min);
}
// loop through each element of the models which is an array of 40 numbers starting from 1980 to 2019
for (model of models) {
  // assign a random make name to make
  make = makes[randomIntFromInterval(0,makes.length-1)]
  // assign a random yaer to model
  model = models[randomIntFromInterval(0,makes.length-1)]
  // initialize a new instance of Model called mycar with above make and model
  mycar = new Model(make, model);
  // print the detail of the instance
  console.log(mycar.show())
}
```