---
id: sanayi-go 

order: 3

title: "SanayiGo | A Supplier-Buyer Platform"

short_description: "A fast B2B mobile commerce platform developed using Flutter and Firebase, enabling suppliers to showcase their products in a mobile environment and buyers to send inquiries about products."

tags: ["Flutter", "Dart", "Firebase", "Firestore", "Mobile Application", "Supply Chain"]

image_gradient_from: "ctp-blue"   
image_gradient_to: "ctp-sapphire" 

icon_class: "fa-solid fa-truck-field"

cover_image: "/assets/images/projects/sanayi-go.png" 

github_url: "https://github.com/SahinMuhammetAbdullah/sanayi_go" 
youtube_url: "https://www.youtube.com/watch?v=2XDAszjixOU"

layout: default
description: "A fast B2B mobile commerce platform developed using Flutter and Firebase, enabling suppliers to showcase their products in a mobile environment and buyers to send inquiries about products."
image: /assets/images/projects/sanayi-go.png
lang: en
---

## Working Principle

SanayiGo is built on a modern, cloud-based architecture that brings suppliers and buyers together in a mobile environment. The application's working principle relies on the integration of a user-experience-focused **Flutter** frontend with the fast and scalable backend services provided by **Firebase**.

### 1. Frontend - Flutter (Dart)

* **Platform:** The mobile interface of the application is developed using **Flutter (Dart)**. This allows it to run on both Android and iOS devices from a single codebase.
* **Architecture:** The project is designed according to **Clean Code** principles for more organized and sustainable development. Pages, services, entities, and components are kept separate.
* **Core Function:** Provides users with all visual interactions such as registration, login, listing products by category, searching, and sending inquiries.

### 2. Backend and Database - Firebase

All backend services for the application are provided by **Google Firebase**, a serverless solution:

* **User Management (Firebase Authentication):** User registration and secure login to the system are managed through this service.
* **Database (Firestore):** Product details (name, price, category, ID) and user information are stored in the **Firestore** NoSQL database. All operations such as adding, deleting, and viewing product details are performed directly through this database.
* **Storage (Firebase Storage):** Product images and media files uploaded by suppliers are stored in this area. Each photo has a unique ID.

### 3. Main Workflow

The platform facilitates communication between two main user roles:

1.  **Supplier (Product Upload):**
    * The supplier enters details such as the product name, category, and price on the **Product Upload** page.
    * The image is added, and the data is uploaded to **Firestore**, while the image is uploaded to **Firebase Storage**.
    * Uploaded products are listed on the user's profile page and can be deleted from there.

2.  **Buyer (Sending Inquiry):**
    * The buyer browses products by category on the main screen or finds the relevant product using the search bar.
    * When they find the desired product, they indicate their interest by pressing the **"Send Inquiry"** button.
    * As a result of this interaction, a notification is immediately sent to the supplier's account who uploaded the product.

This cloud-based structure ensures that the application operates with low latency and can easily scale with an increasing number of users.

