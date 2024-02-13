###QA
**Software Architecture:** Software architecture refers to the fundamental structure of a software system. It's a discipline concerned with the high-level design of the overall system, defining how different components of the system interact with each other. This includes the organization of the system into components, the placement of those components, and the interactions between them. Good software architecture ensures that the system meets its requirements in terms of functionality, performance, maintainability, scalability, and security.

![[Pasted image 20231212111903.png]]

### b) Model View Controller (MVC) Architectural Pattern and Sequence Diagram

**MVC Architectural Pattern:** The Model-View-Controller (MVC) pattern is a widely used architectural pattern in software engineering, particularly in web applications. It divides an application into three interconnected components:

1. **Model:** Manages the data and business logic of the application.
2. **View:** Represents the presentation layer (UI) and displays data to the user.
3. **Controller:** Acts as an interface between Model and View, handling user input and updating the Model and View accordingly.

**Sequence Diagram for MVC:** Here is the sequence diagram illustrating the general runtime behavior of the MVC pattern:

![MVC Sequence Diagram](https://showme.redstarplugin.com/d/d:nqDiEJjF)

### c) MVC Implementation in CS5721 Project

In the CS5721 project, which is an object-oriented Java Spring Boot project, the MVC pattern could be implemented as follows:

- **Model:** Java classes annotated with `@Entity`, representing the application's data model and interacting with the database using Spring Data JPA.
- **View:** Thymeleaf templates or similar technology for rendering the UI. In a RESTful approach, this could also be JSON data sent to a frontend application.
- **Controller:** Spring MVC controllers, annotated with `@Controller`, handling HTTP requests, interacting with the Model, and returning a View.

**Framework Usage:**

- Spring Boot provides a comprehensive platform that supports the MVC architecture with built-in components for each part of the pattern.
- Dependency Injection in Spring Boot helps in managing the dependencies between different components, such as Controllers, Services, and Repositories.
- Spring Data JPA can be used for data persistence in the Model, and Spring MVC for web controllers.
