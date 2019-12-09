# workbook
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


### Q4	A team is about to engage in a project, developing a website for a small business. What knowledge and skills would they need in order to develop the project?

### Q5	With reference to one of your own projects, discuss what knowledge or skills were required to complete your project, and to overcome challenges

### Q6	With reference to one of your own projects, evaluate how effective your knowledge and skills were for this project, and suggest changes or improvements for future projects of a similar nature

### Q7	Explain control flow, using an example from the JavaScript programming language

### Q8	Explain type coercion, using examples from the JavaScript programming language

### Q9	Explain data types, using examples from the JavaScript programming language

### Q10	Explain how arrays can be manipulated in JavaScript, using examples from the JavaScript programming language

### Q11	Explain how objects can be manipulated in JavaScript, using examples from the JavaScript programming language

### Q12	Explain how JSON can be manipulated in JavaScript, using examples from the JavaScript programming language

### Q13	For the code snippet provided below, write comments for each line of code to explain its functionality. In your comments you must demonstrates your ability to recognise and identify functions, ranges and classes


```javascript
class Car {
  constructor(brand) {
    this.carname = brand;
  }
  present() {
    return 'I have a ' + this.carname;
  }
}

class Model extends Car {
  constructor(brand, mod) {
    super(brand);
    this.model = mod;
  }
  show() {
    return this.present() + ', it was made in ' + this.model;
  }
}

let makes = ["Ford", "Holden", "Toyota"]
let models = Array.from(new Array(40), (x,i) => i + 1980)

function randomIntFromInterval(min,max) { // min and max included
    return Math.floor(Math.random()*(max-min+1)+min);
}

for (model of models) {

  make = makes[randomIntFromInterval(0,makes.length-1)]
  model = models[randomIntFromInterval(0,makes.length-1)]
    
  mycar = new Model(make, model);
  console.log(mycar.show())
}
```