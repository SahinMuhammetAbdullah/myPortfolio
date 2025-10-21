---
id: project-lock 

order: 4

title: "Project Lock | Project Management System"

# SHORT DESCRIPTION (Corrected with video content)
short_description: "A desktop project management application developed using C# Forms and MySQL, featuring user-based access control, and project, task, employee management, and status tracking (completed/delayed) features."

# TAGS (Corrected with video content)
tags: ["C# Forms", "Windows Application", "MySQL", "Database Management", "Project Management", "Task Tracking"]

image_gradient_from: "ctp-blue"
image_gradient_to: "ctp-sapphire"

icon_class: "fas fa-lock" # Icon selected to match the project name

cover_image: "/assets/images/projects/project-lock.png"

github_url: "https://github.com/SahinMuhammetAbdullah/ProjectLock"
youtube_url: "https://www.youtube.com/watch?v=GyWu9BpimVg"

layout: default
description: "A desktop project management application developed using C# Forms and MySQL, featuring user-based access control, and project, task, employee management, and status tracking (completed/delayed) features."
image: /assets/images/projects/project-lock.png
lang: en
---

## Working Principle

Project Lock is a desktop application developed on the C# Forms platform that uses an external MySQL database for data management. The main goal of the project is to enable different users (managers) to manage their own projects, employees, and tasks in isolation from other users.

### 1. Core Technology and Architecture

* **Frontend:** The graphical desktop interface where users perform all operations is developed using **C# Forms**.
* **Backend and Database:** All data is stored and managed in a **MySQL** database (MySQL port is opened and controlled via PHPMyAdmin).
* **Connection and Process:** The C# code establishes a connection to MySQL by creating a `connection string` structure and executes all data operations (save, update, delete) using **SQL queries**.

### 2. Data Structure and Relationships

The system contains 4 main tables that form the foundation of project management:

* **User:** Stores basic login information such as `User ID`, `username`, and `password`.
* **Employee:** Includes information like `Employee ID`, first name, last name, number of completed and ongoing projects, and is linked to the `User ID` (Foreign Key).
* **Project:** Contains details such as `Project ID`, name, start date, and end date, and is linked to the `User ID` to identify the owner.
* **Task:** Stores details such as `Task ID`, task name, start date, **man-day value (adam gün değeri)**, end date, and status. This table is linked to the `Employee ID` to indicate who it is assigned to, and to the `User ID` to indicate which user it belongs to.

### 3. Working Principle (User Isolation)

The critical working principle of the project is **User-Based Isolation**:

* Different users (managers) can log into the system with different accounts.
* All tables (`Employee`, `Project`, `Task`) are linked to the **User ID** as a primary key.
* Thanks to this link, when different users log into the system, they **cannot access each other's projects, employees, or tasks**.

### 4. Management Process

* **Project Management:** Users can add a name, start date, and end date to their projects, and list projects.
* **Employee Management:** Employee records can be created, the names/surnames of existing employees can be updated, and their records can be deleted.
* **Task Management and Tracking:** Tasks are added to projects. Man-day values and start/end dates are assigned to these tasks.
* **Status Control:** The deadlines of the tasks are monitored, and the task status (e.g., `completed`) is updated. These updates also affect the number of completed projects for the employee.

