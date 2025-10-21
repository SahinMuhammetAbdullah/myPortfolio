---
id: lazaros-express 

order: 2

title: "Lazaros Express | An E-Commerce Platform"

short_description: "A comprehensive e-commerce platform application developed using a Java-based multi-tier architecture, featuring secure payment and fast order management capabilities."

tags: ["Java", "E-Commerce", "Multi-Tier Architecture", "Database Management", "Web Application"]

image_gradient_from: "ctp-blue"
image_gradient_to: "ctp-sapphire"

icon_class: "fas fa-shopping-cart"

cover_image: "/assets/images/projects/lazaros-express.png"

github_url: "https://github.com/SahinMuhammetAbdullah/lazaros"
youtube_url: "https://www.youtube.com/watch?v=c_bx73bYhsI"

layout: default
description: "A comprehensive e-commerce platform application developed using a Java-based multi-tier architecture, featuring secure payment and fast order management capabilities."
image: /assets/images/projects/lazaros-express.png
lang: en
---

## Working Principle

The Lazaros Express E-Commerce Platform is built on a **Multi-Tier Architecture**, adhering to modern web application development standards. This approach enhances the system's scalability, security, and sustainability. The project is fundamentally built upon the interaction of the following three main layers:

### 1. Presentation Layer

This layer provides the interface with which users directly interact.

* **Role:** Manages user interactions (product search, adding to cart, logging in) and visualizes data received from the Application Layer.
* **Technologies:** Developed using HTML, CSS, JavaScript (and possibly a library/framework like React JS). The `express` folder in the repository may represent the connection point with the web server or APIs for this layer.

### 2. Application/Business Logic Layer

This is the central layer where all e-commerce rules and processes within the system are executed.

* **Role:** Processes requests from the Presentation Layer, enforces necessary business rules (stock control, discount calculation, order validation), and requests/saves data from the Data Layer.
* **Technologies:** Largely developed using the **Java** language. The `Servers` folder in the repository houses the server-side code and business logic for this layer. This layer might have a microservice or modular structure.

### 3. Data Layer

This layer is where all the application's persistent data is securely stored, accessed, and managed.

* **Role:** Responsible for securely storing critical data such as the product catalog, user profiles, order history, and stock levels, and responding to queries from the Application Layer.
* **Technologies:** The presence of the `db` folder indicates that the project uses a database management system (such as PostgreSQL, MySQL, or MongoDB). The application accesses this database using tools like JDBC.

### Summary of Workflow

1.  **Request:** A user performs an action (e.g., "Purchase"). This request is sent as an HTTP request via the Presentation Layer.
2.  **Processing:** The Application Layer captures this request, verifies the user session, and runs the business logic like payment/stock checks.
3.  **Data Communication:** The Business Logic Layer communicates with the Data Layer to create an order record and update stock quantity.
4.  **Response:** With confirmation from the database, the Business Logic Layer completes the process and sends a response back to the Presentation Layer.
5.  **Feedback:** The Presentation Layer displays a message to the user, such as "Your order has been placed."

Thanks to this layered structure, changes to the user interface (Presentation Layer), for example, can be made easily without affecting the backend business logic (Application Layer). This facilitates the maintenance and future scalability of the e-commerce platform.

