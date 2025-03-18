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






