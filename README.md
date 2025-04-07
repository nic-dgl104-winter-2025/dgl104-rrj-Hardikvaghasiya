[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/MMj2nZMu)


# Week 8 - Research and Reflection Journal

## Research a New Language

I explored **Haskell**, a functional programming language widely used in academia, financial modeling, and data analysis. 

- **Use cases:** High-assurance software, mathematical computations.
- **Users:** Researchers, data scientists, and software engineers.
- **Resources:** *Learn You a Haskell for Great Good!* and *Haskell.org* provide structured learning materials.

### JavaScript Example Comparison
To contrast Haskell’s pure functional approach, here’s a JavaScript version of a pure function for summing two numbers:

```js
// Pure function in JavaScript
function sum(a, b) {
  return a + b;
}

console.log(sum(3, 4)); // 7
```

Unlike impure functions, this does not alter external state.

---

## Reflection on Slack Responses

Reading various posts on Slack highlighted the diversity of programming languages. I gained insights into Lua’s efficiency in game development and Processing’s accessibility for creative coding. One thing that stood out was how user-centered language communities are, with Lua heavily supported in the game dev community, and Processing in visual arts and education.

---

## User Story for Spotify

- *"As a user, I can create a playlist and add songs to it."*
- *"As a user, I can share my playlist with friends."*
- *"As a user, I can remove songs from my playlist."*

**Acceptance Criteria:**
- The playlist feature should have a clear 'Create Playlist' button.
- Users should be able to search and add songs easily.
- A straightforward delete option should be available for removing songs.

### JavaScript Example: Playlist Feature Logic

```js
// Playlist logic in JavaScript
class Playlist {
  constructor(name) {
    this.name = name;
    this.songs = [];
  }

  addSong(song) {
    this.songs.push(song);
  }

  removeSong(title) {
    this.songs = this.songs.filter(song => song.title !== title);
  }
}

const myPlaylist = new Playlist("Workout Mix");
myPlaylist.addSong({ title: "Thunderstruck", artist: "AC/DC" });
myPlaylist.addSong({ title: "Stronger", artist: "Kanye West" });
myPlaylist.removeSong("Thunderstruck");
console.log(myPlaylist);
```

---

## Choosing a Programming Language for the Project

**Selected Language:** **React Native**

- **Experience Level:** Moderate (one semester + personal projects).
- **Reason for Choice:** Allows for cross-platform mobile app development, providing flexibility and community support.

---

## Exploring GitHub Repositories

Exploring open-source projects on GitHub revealed:
- Extensive **React Native** repositories for mobile development.
- **Functional programming applications** in Haskell that reduce side effects.
- UI/UX projects focusing on responsive, accessible design.

### GitHub Example with JavaScript
```js
// Example of exploring starred repositories via GitHub REST API (token needed)
fetch("https://api.github.com/users/{username}/starred")
  .then(res => res.json())
  .then(data => console.log("Starred Repositories:", data));
```

---

## Reflection

1. **Key Insight:** Haskell’s functional nature reduces bugs, making it ideal for high-reliability systems.
2. **Alternative Languages for DGL 104:** TypeScript and Dart due to strong typing, scalability, and mobile/web support.
3. **GitHub Observations:** Projects emphasize modularity and efficiency. Starred repositories often follow clean architecture and good documentation practices.

---

## References

- Blacquiere, A. (2024). *DGL 104 Application Development Foundations*. Retrieved from Brightspace.
- *Learn You a Haskell for Great Good!* (Haskell Tutorial). Retrieved from [http://learnyouahaskell.com](http://learnyouahaskell.com)
- Haskell.org. Official Documentation. Retrieved from [https://www.haskell.org/](https://www.haskell.org/)
- Mozilla Developer Network. JavaScript Docs:
  - [filter()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)
  - [map()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map)
  - [reduce()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce)
  - [sort()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/sort)
- GitHub Docs: [GitHub Explore](https://github.com/explore)
- React Native Docs: [https://reactnative.dev](https://reactnative.dev)
- Lua.org. Official Docs. Retrieved from [https://www.lua.org](https://www.lua.org)
- Processing.org: Creative coding in Processing. Retrieved from [https://processing.org](https://processing.org)
- Dev.to (2023). *Unlocking the Power of Functional Programming*. Retrieved from [https://dev.to](https://dev.to)
- Medium (2024). *Functional JavaScript and Modern App Development*. Retrieved from [https://medium.com](https://medium.com)



# Week 9 - Research and Reflection Journal


### **Research on Design Patterns**
Design patterns are reusable solutions to common programming challenges. I researched four key design patterns:

1. **Singleton Pattern**
   - **Purpose:** Ensures a class has only one instance and provides a global access point.
   - **Real-world Application:** Used in logging services or shared configuration systems.
   - **Code Example (JavaScript):**
     ```javascript
     class Singleton {
         constructor() {
             if (!Singleton.instance) {
                 this.theme = "dark";
                 Singleton.instance = this;
             }
             return Singleton.instance;
         }

         getTheme() {
             return this.theme;
         }

         setTheme(newTheme) {
             this.theme = newTheme;
         }
     }

     const app1 = new Singleton();
     const app2 = new Singleton();
     console.log(app1 === app2); // true
     app1.setTheme("light");
     console.log(app2.getTheme()); // "light"
     ```
   - **Reference:** [Wikipedia - Singleton Pattern](https://en.wikipedia.org/wiki/Singleton_pattern), [Learning JS Design Patterns - Addy Osmani](https://addyosmani.com/resources/essentialjsdesignpatterns/book/), [GeeksForGeeks - Singleton in JavaScript](https://www.geeksforgeeks.org/singleton-design-pattern/)

2. **Factory Pattern**
   - **Purpose:** Provides an interface for creating objects without specifying their concrete class.
   - **Real-world Application:** Object creation based on user input in games or form builders.
   - **Code Example (JavaScript):**
     ```javascript
     class Developer {
         constructor(name) {
             this.name = name;
             this.role = "Developer";
         }
     }

     class Tester {
         constructor(name) {
             this.name = name;
             this.role = "Tester";
         }
     }

     function employeeFactory(role, name) {
         if (role === "dev") return new Developer(name);
         if (role === "test") return new Tester(name);
         throw new Error("Invalid role");
     }

     const emp1 = employeeFactory("dev", "Alice");
     const emp2 = employeeFactory("test", "Bob");
     console.log(emp1, emp2);
     ```
   - **Reference:** [Wikipedia - Factory Method Pattern](https://en.wikipedia.org/wiki/Factory_method_pattern), [Refactoring Guru - Factory](https://refactoring.guru/design-patterns/factory-method), [DigitalOcean](https://www.digitalocean.com/community/tutorials/js-design-patterns-factory)

3. **Observer Pattern**
   - **Purpose:** Defines a one-to-many dependency between objects so that when one changes, all dependents are notified.
   - **Real-world Application:** News subscriptions, UI frameworks (e.g., event listeners).
   - **Code Example (JavaScript):**
     ```javascript
     class Subject {
         constructor() {
             this.observers = [];
         }
         subscribe(observer) {
             this.observers.push(observer);
         }
         unsubscribe(observer) {
             this.observers = this.observers.filter(obs => obs !== observer);
         }
         notify(data) {
             this.observers.forEach(obs => obs.update(data));
         }
     }

     class Observer {
         constructor(name) {
             this.name = name;
         }
         update(data) {
             console.log(`${this.name} received update: ${data}`);
         }
     }

     const subject = new Subject();
     const o1 = new Observer("A");
     const o2 = new Observer("B");
     subject.subscribe(o1);
     subject.subscribe(o2);
     subject.notify("Update 1");
     ```
   - **Reference:** [Wikipedia - Observer Pattern](https://en.wikipedia.org/wiki/Observer_pattern), [Refactoring Guru - Observer](https://refactoring.guru/design-patterns/observer), [JavaScript Info - Observers](https://javascript.info/custom-events)

4. **Decorator Pattern**
   - **Purpose:** Adds additional responsibilities to an object dynamically without modifying its structure.
   - **Real-world Application:** Enhancing UI elements (e.g., applying styles dynamically).
   - **Code Example (JavaScript):**
     ```javascript
     class Coffee {
         getCost() { return 5; }
         getDescription() { return "Plain Coffee"; }
     }

     class MilkDecorator {
         constructor(coffee) {
             this.coffee = coffee;
         }
         getCost() {
             return this.coffee.getCost() + 1;
         }
         getDescription() {
             return this.coffee.getDescription() + ", Milk";
         }
     }

     let myCoffee = new Coffee();
     myCoffee = new MilkDecorator(myCoffee);
     console.log(myCoffee.getDescription(), myCoffee.getCost());
     ```
   - **Reference:** [Wikipedia - Decorator Pattern](https://en.wikipedia.org/wiki/Decorator_pattern), [Refactoring Guru - Decorator](https://refactoring.guru/design-patterns/decorator), [freeCodeCamp Decorator Tutorial](https://www.freecodecamp.org/news/javascript-design-patterns-decorator/)

### **Reflection on Open Source Contributions**
- GitHub's guide taught me that documentation updates, bug fixing, and feature suggestions are all valuable contributions.
- I found that many projects prioritize modularity and clarity, making collaboration easier.
- Reference: [GitHub Open Source Guide](https://opensource.guide/)

### **Application Development Coding Project**
- Our team created a GitHub repo and shared it with the instructor.
- We are refining project goals and establishing a workflow.

### **Issue Identification & Slack Summary**
- I identified an issue related to accessibility in a React Native UI library.
- It’s a meaningful opportunity because it directly impacts usability and inclusivity.

### **Follow-up Questions & Reflection**
1. **Language Confirmation:** React Native still aligns with our goals due to its cross-platform advantages.
2. **Project Timeline:** We’ve outlined milestones and assigned initial tasks.
3. **Open Source Learnings:** Emphasized the need for clear issues, good first issues, and the importance of communication.

---

## References
- *Learning JavaScript Design Patterns* by Addy Osmani. Retrieved from [https://addyosmani.com/resources/essentialjsdesignpatterns/book/](https://addyosmani.com/resources/essentialjsdesignpatterns/book/)
- *Refactoring Guru - Design Patterns*. Retrieved from [https://refactoring.guru/design-patterns](https://refactoring.guru/design-patterns)
- GitHub Open Source Guide. Retrieved from [https://opensource.guide/](https://opensource.guide/)
- Wikipedia - [Singleton](https://en.wikipedia.org/wiki/Singleton_pattern), [Factory](https://en.wikipedia.org/wiki/Factory_method_pattern), [Observer](https://en.wikipedia.org/wiki/Observer_pattern), [Decorator](https://en.wikipedia.org/wiki/Decorator_pattern)
- Patterns.dev. Design Patterns in JavaScript. Retrieved from [https://www.patterns.dev](https://www.patterns.dev)
- GeeksForGeeks - [Singleton in JavaScript](https://www.geeksforgeeks.org/singleton-design-pattern/)
- DigitalOcean - [Factory Pattern](https://www.digitalocean.com/community/tutorials/js-design-patterns-factory)
- JavaScript Info - [Custom Events & Observer](https://javascript.info/custom-events)
- freeCodeCamp - [JavaScript Decorator Pattern](https://www.freecodecamp.org/news/javascript-design-patterns-decorator/)
- DEV Community - [OOP Design Patterns in JavaScript](https://dev.to/azure/oop-design-patterns-in-javascript-4m9h)
- Medium - [Explaining JavaScript Design Patterns](https://medium.com/javascript-scene/design-patterns-explained-with-javascript-7e8f7e6da2d)
- Codeburst - [10 Common JavaScript Design Patterns](https://codeburst.io/10-common-javascript-design-patterns-3d9f9dbc1e5c)


---
# Week 10 - Research and Reflection Journal

## MV* Architecture: Overview and Key Insights

This week I delved into MV* architectural patterns, shorthand for "Model-View-Whatever." MV* refers to a family of design patterns that separate an application into Models, Views, and some mediator (Controller, Presenter, ViewModel, etc.) ([StackOverflow, 2023](https://stackoverflow.com/questions/34828252/what-does-the-star-mean-in-mv)). The lecture emphasized that all MV* patterns share the goal of separating concerns – managing data, rendering UI, and processing input independently. According to Chirag Aggarwal, MVC, MVP, and MVVM focus on organizing code within an application by separating the data (Model), UI (View), and interaction logic ([Dev.to, 2021](https://dev.to/chiragagg5/mvc-mvp-and-mvvm-design-patterns-3h3a)).

The lecture and Addy Osmani's writings further explain the main differences between MVC, MVP, and MVVM: how layers interact and depend on each other ([Osmani, 2012](https://addyosmani.com/resources/essentialjsdesignpatterns/book/#detailmvcmvpandmvvm)). For example, MVVM uses a ViewModel to handle all communication between Model and View. In contrast, MVC uses a Controller as the mediator. All MV* patterns aim to create cleaner, modular, and testable applications.

---

## Model-View-Controller (MVC) Pattern

MVC breaks applications into three components:

- **Model**: Handles business logic and data ([Rascia, 2020](https://www.taniarascia.com/javascript-mvc-todo-app/)).
- **View**: Manages the presentation layer and UI ([Rascia, 2020](https://www.taniarascia.com/javascript-mvc-todo-app/)).
- **Controller**: Connects user input to model updates and view rendering ([Rascia, 2020](https://www.taniarascia.com/javascript-mvc-todo-app/)).

The model and view should never directly interact. The controller mediates all updates, allowing for modular and maintainable applications ([Rascia, 2020](https://www.taniarascia.com/javascript-mvc-todo-app/)).

**JavaScript MVC Example:**
```javascript
class Model {
  constructor() {
    this.todos = [];
  }
  addTodo(item) {
    this.todos.push(item);
  }
}

class View {
  constructor() {
    this.form = document.querySelector('#todo-form');
    this.input = document.querySelector('#todo-input');
    this.list = document.querySelector('#todo-list');
  }
  displayTodos(todos) {
    this.list.innerHTML = todos.map(todo => `<li>${todo.text}</li>`).join('');
  }
  bindAddTodo(handler) {
    this.form.addEventListener('submit', event => {
      event.preventDefault();
      if (this.input.value) {
        handler(this.input.value);
        this.input.value = "";
      }
    });
  }
}

class Controller {
  constructor(model, view) {
    this.model = model;
    this.view = view;
    this.view.displayTodos(this.model.todos);
    this.view.bindAddTodo(this.handleAddTodo);
  }
  handleAddTodo = (todoText) => {
    this.model.addTodo({ text: todoText, complete: false });
    this.view.displayTodos(this.model.todos);
  };
}

const app = new Controller(new Model(), new View());
```

---

## Model-View-ViewModel (MVVM) Pattern

MVVM also separates application layers:
- **Model**: Represents application data ([Medium, 2023](https://medium.com/)).
- **View**: Displays UI and is passive ([Dev.to, 2021](https://dev.to/makanjuoreoluwa/react-and-mvvm-separating-ui-and-logic-2p1e)).
- **ViewModel**: Exposes model data and logic for the view, handling state and commands ([Osmani, 2012](https://addyosmani.com/resources/essentialjsdesignpatterns/book/#detailmvcmvpandmvvm)).

A core advantage of MVVM is **data binding** – a two-way link between the ViewModel and View, ensuring the UI auto-updates with model changes and vice versa.

**React MVVM Example:**
```jsx
class TaskModel {
  constructor() {
    this.tasks = [];
  }
  addTask(task) {
    this.tasks.push(task);
  }
  getAllTasks() {
    return this.tasks;
  }
}

import { useState } from 'react';
function useTaskViewModel() {
  const [taskModel] = useState(() => new TaskModel());
  const addTask = (taskText) => {
    taskModel.addTask(taskText);
  };
  const getAllTasks = () => taskModel.getAllTasks();
  return { addTask, getAllTasks };
}

function TaskApp() {
  const [input, setInput] = useState("");
  const [tasks, setTasks] = useState([]);
  const { addTask, getAllTasks } = useTaskViewModel();

  const handleAdd = () => {
    addTask(input);
    setInput("");
    setTasks(getAllTasks());
  };

  return (
    <div>
      <h1>Tasks</h1>
      <input value={input} onChange={(e) => setInput(e.target.value)} />
      <button onClick={handleAdd}>Add Task</button>
      <ul>
        {tasks.map((task, idx) => <li key={idx}>{task}</li>)}
      </ul>
    </div>
  );
}
```

This pattern simplifies testing and separation of logic ([BrightMarbles, 2023](https://brightmarbles.io/)).

---

## MV* in React + MongoDB (MERN Stack)

In my MERN stack project:
- **MVC** is applied to the backend:
  - Model = MongoDB/Mongoose schemas
  - View = React frontend
  - Controller = Express API routes ([Medium, 2023](https://medium.com/))

- **MVVM** fits the frontend:
  - View = React components
  - ViewModel = Contexts/hooks with logic and state
  - Model = API service or backend

As discussed on Reddit, React can be considered the VVM of MVVM, while the Model is implemented through services or external logic ([Reddit, 2022](https://www.reddit.com/))

---


## Reflection: Challenges and Solutions

### Challenge
Understanding and applying MVVM in React without two-way binding.

### Solution
- Used external tutorials to experiment ([Dev.to, 2021](https://dev.to/makanjuoreoluwa/react-and-mvvm-separating-ui-and-logic-2p1e))
- Asked a classmate for architectural guidance
- Broke the problem into small use-cases

---

## References
- Stack Overflow. (2023). [MV* architecture definition](https://stackoverflow.com/questions/34828252/what-does-the-star-mean-in-mv)
- Dev.to. (2021). Chirag Aggarwal, [MVC, MVP, MVVM](https://dev.to/chiragagg5/mvc-mvp-and-mvvm-design-patterns-3h3a)
- Osmani, A. (2012). [JavaScript Design Patterns](https://addyosmani.com/resources/essentialjsdesignpatterns/book/#detailmvcmvpandmvvm)
- Rascia, T. (2020). [JavaScript MVC Example](https://www.taniarascia.com/javascript-mvc-todo-app/)
- Medium. (2023). [MVVM in Web Development](https://medium.com/)
- Dev.to. (2021). Makanju O. [React + MVVM guide](https://dev.to/makanjuoreoluwa/react-and-mvvm-separating-ui-and-logic-2p1e)
- BrightMarbles. (2023). [MVVM Testing Benefits](https://brightmarbles.io/)
- Reddit. (2022). [MVVM in React Discussion](https://www.reddit.com/)



# Week 11 – Object-Oriented Programming

## Research and Reflection

### Object-Oriented Programming vs Functional Programming: Key Concepts from the Videos
The two lecture videos this week provided a comparison between object-oriented programming (OOP) and functional programming. OOP focuses on organizing code into objects that bundle state (data) and behavior (methods). Functional programming, by contrast, emphasizes the use of pure functions and immutable data (YouTube, "Object-Oriented Programming vs Functional Programming"). While OOP allows state to be modified through methods on objects, functional programming avoids side effects, instead relying on predictable, pure function composition.

JavaScript, as a multi-paradigm language, supports both OOP and functional styles. This was clearly shown in the videos, which argued that blending these paradigms often produces better code. For example, React has evolved from class-based (OOP) components to functional components using Hooks. This reflects a shift toward combining the strengths of both paradigms (YouTube, "JavaScript OOP: Encapsulation, Abstraction, Inheritance, and Polymorphism").

### The Four Pillars of OOP in JavaScript

#### Encapsulation
Encapsulation involves hiding an object’s internal state and only exposing access through defined methods. This promotes modularity and prevents unintended interference with the object’s data.
```js
class Car {
  constructor(brand) {
    this._brand = brand;
  }
  get brand() {
    return this._brand;
  }
  set brand(newBrand) {
    this._brand = newBrand;
  }
}
```
(MDN, "Encapsulation – Glossary")

#### Abstraction
Abstraction hides complexity by exposing only necessary components. For example, a `Vehicle` class might have general methods like `startEngine()` without showing how the engine works.
```js
class Vehicle {
  startEngine() {
    console.log("Engine started");
  }
}
```
(MDN, "Abstraction – Glossary")

#### Inheritance
Inheritance allows classes to reuse properties and methods of other classes.
```js
class Animal {
  speak() {
    console.log("Animal speaks");
  }
}
class Dog extends Animal {
  speak() {
    console.log("Dog barks");
  }
}
```
(MDN, "Object-Oriented Programming")

#### Polymorphism
Polymorphism allows the same method to behave differently depending on the object.
```js
function makeAnimalSpeak(animal) {
  animal.speak();
}
makeAnimalSpeak(new Dog());  // Dog barks
```


### OOP in React.js and Project Implementation
In React, OOP principles can be seen in both class and functional components. Class components encapsulate state and behavior, supporting encapsulation and inheritance via `React.Component`. Although React now prefers composition over inheritance, the essence of OOP remains through component encapsulation and reuse (React Documentation).

On the backend, Mongoose provides an object model for MongoDB. Models created with Mongoose encapsulate schema logic and abstract database operations. This illustrates how OOP patterns like encapsulation and abstraction are used in a full-stack JavaScript project.

### JavaScript as a Multi-Paradigm Language
JavaScript supports both OOP and functional programming. Functions are first-class citizens, but the language also provides prototype-based and class-based OOP features. Developers can use the paradigm best suited to the task (MDN, "Object-Oriented Programming").

### Best Practices and Real-World Applications
Best practices in OOP include:
- Favoring composition over inheritance (React Documentation).
- Designing clear and abstract interfaces.
- Using design patterns like Singleton and Observer where appropriate (Merced).
- Following SOLID principles for maintainable architecture.

For example, the Observer pattern is used in event systems, and the Singleton pattern can be used to manage a single database connection in Node.js (Merced).

### Community and Open-Source Reflections
Engaging with the open-source community was encouraged this week. I contributed to a GitHub repository by fixing documentation and asked a question on Stack Overflow about Mongoose schemas. This interaction highlighted how open source encourages collaborative problem-solving and aligns with course goals (Elliott).

---

## References

- Blacquiere, Ashley. *DGL 104 Application Development Foundations*. Brightspace, 2025.
- Mozilla Developer Network (MDN). “Encapsulation – Glossary.” *MDN Web Docs*, Mozilla, 8 June 2023, [https://developer.mozilla.org/en-US/docs/Glossary/Encapsulation](https://developer.mozilla.org/en-US/docs/Glossary/Encapsulation).
- Mozilla Developer Network (MDN). “Abstraction – Glossary.” *MDN Web Docs*, Mozilla, 6 May 2024, [https://developer.mozilla.org/en-US/docs/Glossary/Abstraction](https://developer.mozilla.org/en-US/docs/Glossary/Abstraction).
- Mozilla Developer Network (MDN). “Object-oriented programming.” *MDN Web Docs*, Mozilla, 6 Mar. 2025, [https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Object-oriented_programming](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Object-oriented_programming).
- React Documentation. “Composition vs Inheritance.” *React.js Docs*, Meta, [https://reactjs.org/docs/composition-vs-inheritance.html](https://reactjs.org/docs/composition-vs-inheritance.html).
- Zalewski, Bart. “Object-Oriented Programming in JavaScript with Examples (Updated 2024).” *Medium*, 2024, [https://medium.com/@bzalewski/object-oriented-programming-in-javascript](https://medium.com/@bzalewski/object-oriented-programming-in-javascript).
- Elliott, Eric. “The Forgotten History of OOP.” *JavaScript Scene*, Medium, 2016, [https://medium.com/javascript-scene/the-forgotten-history-of-oop-88d71b9b2bfc](https://medium.com/javascript-scene/the-forgotten-history-of-oop-88d71b9b2bfc).
- Merced, Alex. “OOP Design Patterns in JavaScript.” *DEV Community*, 2023, [https://dev.to/azure/oop-design-patterns-in-javascript-4m9h](https://dev.to/azure/oop-design-patterns-in-javascript-4m9h).
- YouTube. “Object-Oriented Programming vs Functional Programming.” *YouTube*, uploaded by Tech with Tim, [https://youtu.be/hdVYcOgNKfc](https://youtu.be/hdVYcOgNKfc).
- YouTube. “JavaScript OOP: Encapsulation, Abstraction, Inheritance, and Polymorphism.” *YouTube*, uploaded by BroCode, [https://youtu.be/jzP2sw3I1nc](https://youtu.be/jzP2sw3I1nc).

---

## Week 12 – Functional Programming

### Imperative vs. Declarative Paradigms

In **imperative programming**, the code describes *how* to do something – it uses statements that change a program’s state step by step ([Wikipedia - Imperative programming](https://en.wikipedia.org/wiki/Imperative_programming)).

By contrast, **declarative programming** focuses on *what outcome* is desired, not the exact steps to get there ([Wikipedia - Declarative programming](https://en.wikipedia.org/wiki/Declarative_programming)). Functional programming falls under this category. Declarative approaches often eliminate side effects and are more expressive of the problem logic.

### The Functional Programming Paradigm

**Functional programming (FP)** builds programs by applying and composing functions. It's declarative, emphasizes **pure functions**, **immutability**, and **higher-order functions**, and avoids shared state ([Wikipedia - Functional programming](https://en.wikipedia.org/wiki/Functional_programming)).

Key traits:

- Functions are **first-class**: passable as values.
- Functions are **pure**: no side effects.
- Avoids mutable data.

Benefits include simplicity, testability, and easier reasoning ([Medium](https://medium.com)).

### Pure Functions and Side Effects

A **pure function**:

1. Always returns the same output for the same input.
2. Has no side effects ([Wikipedia - Pure function](https://en.wikipedia.org/wiki/Pure_function)).

**Side effects** include modifying global state, printing, or performing I/O.

**Referential transparency** means expressions can be replaced with their values without changing program behavior ([Wikipedia - Referential transparency](https://en.wikipedia.org/wiki/Referential_transparency)).

### Higher-Order Functions (HOFs)

A **higher-order function** takes/returns another function ([Wikipedia - Higher-order function](https://en.wikipedia.org/wiki/Higher-order_function)).

JavaScript supports this via:

#### `filter()`

```js
const numbers = [1, 2, 3, 4, 5];
const evens = numbers.filter(x => x % 2 === 0);
console.log(evens); // [2, 4]
```

[MDN - filter()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)

#### `map()`

```js
const nums = [1, 2, 3, 4];
const squares = nums.map(n => n * n);
console.log(squares); // [1, 4, 9, 16]
console.log(nums);    // [1, 2, 3, 4]
```

[MDN - map()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map)

#### `reduce()`

```js
const values = [5, 10, 15];
const total = values.reduce((acc, curr) => acc + curr, 0);
console.log(total); // 30
```

[MDN - reduce()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce)

#### `sort()`

```js
const names = ["Charlie", "alice", "Bob"];
names.sort();
console.log(names); // ["Bob", "Charlie", "alice"]

names.sort((a, b) => a.localeCompare(b, undefined, { sensitivity: 'base' }));
console.log(names); // ["alice", "Bob", "Charlie"]
```

[MDN - sort()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/sort)

### Recursion

Used to break a problem into smaller sub-problems ([Wikipedia - Recursion](https://en.wikipedia.org/wiki/Recursion_\(computer_science\))).

#### Example:

```js
function factorial(n) {
  if (n <= 1) return 1;
  return n * factorial(n - 1);
}
console.log(factorial(5)); // 120
```

### Functional Programming in Multi-Paradigm Languages

**JavaScript**: Supports FP through first-class functions, array methods, and libraries like Lodash ([iq.js.org](https://iq.js.org)).

**Kotlin**: Offers lambdas, HOFs, and collection operations ([Medium - Kotlin FP](https://medium.com)).

**Swift**: Features `map`, `filter`, `reduce`, closures, and lazy sequences ([Wikipedia - Swift](https://en.wikipedia.org/wiki/Swift_\(programming_language\))).

Others include Python, Java (Streams), and C# (LINQ).

### Benefits of Functional List Operations

- **Clarity**: Express what, not how ([Medium](https://medium.com), [Dev.to](https://dev.to)).
- **Immutability**: No unintended side effects ([Wikipedia - Functional programming](https://en.wikipedia.org/wiki/Functional_programming)).
- **Modularity**: Composable functions ([Dev.to](https://dev.to)).
- **Testability**: Easy to test pure functions.
- **Parallelism**: Safe concurrent operations ([Dev.to - FP](https://dev.to)).
- **Explicit State**: State is passed, not mutated.

### References

- [Imperative programming](https://en.wikipedia.org/wiki/Imperative_programming)
- [Declarative programming](https://en.wikipedia.org/wiki/Declarative_programming)
- [Functional programming](https://en.wikipedia.org/wiki/Functional_programming)
- [Pure function](https://en.wikipedia.org/wiki/Pure_function)
- [Higher-order function](https://en.wikipedia.org/wiki/Higher-order_function)
- [Array.prototype.filter() - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)
- [Array.prototype.map() - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map)
- [Array.prototype.reduce() - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce)
- [Array.prototype.sort() - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/sort)
- [Recursion - Wikipedia](https://en.wikipedia.org/wiki/Recursion_\(computer_science\))
- [JS Paradigms](https://iq.js.org)
- [Kotlin & FP - Medium](https://medium.com)
- [Swift](https://en.wikipedia.org/wiki/Swift_\(programming_language\))
- [Dev.to FP Benefits](https://dev.to)

