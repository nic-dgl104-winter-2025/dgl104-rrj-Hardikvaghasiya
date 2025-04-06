[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/MMj2nZMu)


# Week 8 - Research and Reflection Journal


### **Research a New Language**
I explored **Haskell**, a functional programming language widely used in academia, financial modeling, and data analysis. 
- **Use cases:** High-assurance software, mathematical computations.
- **Users:** Researchers, data scientists, and software engineers.
- **Resources:** *Learn You a Haskell for Great Good!* and *Haskell.org* provide structured learning materials.

### **Reflection on Slack Responses**
Reading various posts on Slack highlighted the diversity of programming languages. I gained insights into Lua’s efficiency in game development and Processing’s accessibility for creative coding.

### **User Story for Spotify**
- *"As a user, I can create a playlist and add songs to it."*
- *"As a user, I can share my playlist with friends."*
- *"As a user, I can remove songs from my playlist."*

**Acceptance Criteria:**
- The playlist feature should have a clear 'Create Playlist' button.
- Users should be able to search and add songs easily.
- A straightforward delete option should be available for removing songs.

### **Choosing a Programming Language for the Project**
**Selected Language:** **React Native**
- **Experience Level:** Moderate (one semester + personal projects).
- **Reason for Choice:** Allows for cross-platform mobile app development, providing flexibility.

### **Exploring GitHub Repositories**
Exploring open-source projects on GitHub revealed:
- Extensive **React Native repositories** for mobile development.
- Functional programming applications for expanding Haskell knowledge.
- UI/UX projects emphasizing user-friendly design.

### **Reflection**
1. **Key Insight:** Haskell’s functional nature reduces bugs, making it suitable for high-reliability software.
2. **Alternative Languages for DGL 104:** TypeScript and Dart due to their strong typing and mobile capabilities.
3. **GitHub Observations:** Open-source projects emphasize modularity and efficiency, showcasing best practices in collaborative coding.

---

## References
- Blacquiere, A. (2024). *DGL 104 Application Development Foundations*. Retrieved from Brightspace.
- *Learn You a Haskell for Great Good!* (Haskell Tutorial). Retrieved from [http://learnyouahaskell.com](http://learnyouahaskell.com)
- Haskell.org. Official Documentation. Retrieved from [https://www.haskell.org/](https://www.haskell.org/)
- GitHub Explore. Open-source repository insights. Retrieved from [https://github.com/explore](https://github.com/explore)

---

# Week 9 - Research and Reflection Journal


### **Research on Design Patterns**
Design patterns are reusable solutions to common programming challenges. I researched four key design patterns:

1. **Singleton Pattern**
   - **Purpose:** Ensures a class has only one instance and provides a global access point.
   - **Real-world Application:** Used in database connection management.
   - **Example:** A logging service that maintains a single instance throughout an application.
   - **Code Example (JavaScript):**
     ```javascript
     class Singleton {
         constructor() {
             if (!Singleton.instance) {
                 Singleton.instance = this;
             }
             return Singleton.instance;
         }
     }

     const instance1 = new Singleton();
     const instance2 = new Singleton();
     console.log(instance1 === instance2); // Output: true
     ```

2. **Factory Pattern**
   - **Purpose:** Provides an interface for creating objects, allowing subclasses to alter object creation.
   - **Real-world Application:** Common in frameworks like Angular and Spring Boot.
   - **Example:** A vehicle factory that creates different car models based on user input.
   - **Code Example (JavaScript):**
     ```javascript
     class Car {
         constructor(model) {
             this.model = model;
         }
     }

     class CarFactory {
         static createCar(model) {
             return new Car(model);
         }
     }

     let myCar = CarFactory.createCar("Sedan");
     console.log(myCar.model); // Output: Sedan
     ```

3. **Observer Pattern**
   - **Purpose:** Defines a dependency between objects so that when one object changes, others are notified.
   - **Real-world Application:** Used in event-driven programming like GUI applications.
   - **Example:** A news subscription service where users receive updates when new articles are published.
   - **Code Example (JavaScript):**
     ```javascript
     class NewsPublisher {
         constructor() {
             this.subscribers = [];
         }
         subscribe(subscriber) {
             this.subscribers.push(subscriber);
         }
         notify(news) {
             this.subscribers.forEach(sub => sub.update(news));
         }
     }

     class Subscriber {
         update(news) {
             console.log(`Breaking News: ${news}`);
         }
     }

     let publisher = new NewsPublisher();
     let user1 = new Subscriber();
     publisher.subscribe(user1);
     publisher.notify("New article published!");
     ```

4. **Decorator Pattern**
   - **Purpose:** Adds additional responsibilities to an object dynamically without modifying its structure.
   - **Real-world Application:** Used in UI development for dynamically adding behaviors.
   - **Example:** A text editor where users can apply different styles like bold or italic dynamically.
   - **Code Example (JavaScript):**
     ```javascript
     function boldDecorator(textFunction) {
         return function() {
             return `<b>${textFunction()}</b>`;
         };
     }

     function getText() {
         return "Hello, world!";
     }

     const decoratedText = boldDecorator(getText);
     console.log(decoratedText()); // Output: <b>Hello, world!</b>
     ```

### **Reflection on Open Source Contributions**
I explored GitHub’s "How to Contribute to Open Source" guide and learned about different contribution methods:
- **Documentation Improvements:** Many open-source projects need better documentation.
- **Bug Fixing:** Fixing minor issues is a great way to start contributing.
- **Feature Requests & Implementations:** Adding new functionalities based on user feedback.

I also explored open-source repositories and noted that many projects emphasize **modularity** and **code readability**, making collaboration easier.

### **Application Development Coding Project**
- Our group has set up a GitHub repository and shared the link with you.
- We are discussing project requirements and establishing a development workflow.

### **Issue Identification & Slack Summary**
I identified an issue in an open-source repository that aligns with my interests. The repository focuses on React Native UI components, and the issue involves improving the accessibility of a navigation bar. I shared my findings on Slack, including a link to the issue and why I believe it is a good contribution opportunity.

### **Follow-up Questions & Reflection**
1. **Is React Native still the best choice?** Yes, because of its cross-platform capabilities and ease of use.
2. **Application Development Plan:** We are drafting a project timeline with key milestones to meet deadlines.
3. **Observations from GitHub Contributions:** Open-source projects require clear issue tracking and collaboration, making communication essential for success.

---

## References
- *Learning JavaScript Design Patterns* by Addy Osmani. Retrieved from [https://addyosmani.com/resources/essentialjsdesignpatterns/book/](https://addyosmani.com/resources/essentialjsdesignpatterns/book/)
- *Refactoring Guru - Design Patterns*. Retrieved from [https://refactoring.guru/design-patterns](https://refactoring.guru/design-patterns)
- GitHub Open Source Guide. Retrieved from [https://opensource.guide/](https://opensource.guide/)

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









