# Task 1 – Spring Boot Application

## Project Overview

This project is a simple Spring Boot application created for Task 1.
It demonstrates the basic functionality of a Spring application, including handling HTTP requests, returning responses, and displaying a web page using the MVC pattern.

---
#

## Objectives

The main goals of this project were:

* Create a Spring Boot project from scratch
* Implement a controller to handle HTTP requests
* Use `@ResponseBody` to return plain text
* Return an HTML view using Thymeleaf (MVC pattern)
* Serve static resources (image)

---

## Technologies Used

* Java
* Spring Boot
* Spring Web
* Thymeleaf
* Maven

---

## How to Run the Application

1. Open the project in IntelliJ IDEA (or any IDE)
2. Make sure Maven dependencies are loaded
3. Run the main class:

   ```
   Task1Application.java
   ```
4. Open your browser and go to:

   ```
   http://localhost:8080
   ```

---

## Application Features

### 🔹 1. Controller with @ResponseBody

The application initially uses a controller that returns a plain text response.

Example:

```
Hello, Task 1 is working!
```

This demonstrates:

* Handling HTTP GET requests
* Using `@ResponseBody` to return data directly

---

### 🔹 2. MVC Pattern (Thymeleaf View)

The application is extended to return an HTML page instead of plain text.

* HTML file: `greeting.html`
* Location: `src/main/resources/templates`

The controller returns:

```
greeting
```

Spring Boot automatically maps this to:

```
templates/greeting.html
```

---

### 🔹 3. Static Resources (Image)

An image is displayed on the webpage.

* Location: `src/main/resources/static`
* Access path: `/vistula.png`

To ensure the application works even if the image is missing, a fallback image is used.

Example:

```html
<img src="/vistula.png" alt="Vistula Logo"
     onerror="this.onerror=null; this.src='https://upload.wikimedia.org/wikipedia/commons/thumb/6/6b/Placeholder.svg/512px-Placeholder.svg.png';">
```

---

## Testing the Application

To test the application:

1. Run the project
2. Open a browser
3. Go to:

   ```
   http://localhost:8080
   ```

Expected result:

* A web page is displayed
* Text content is visible
* Image is shown (or fallback image if missing)

---

## Project Structure

```
src
 └── main
     ├── java
     │    └── com.racheal.task1
     │         └── controller
     │              └── HelloController.java
     └── resources
          ├── templates
          │     └── greeting.html
          └── static
                └── vistula.png
```

---


---

## Summary

This project demonstrates:

* Basic Spring Boot configuration
* Creating and running a web application
* Handling HTTP requests using a controller
* Returning responses using `@ResponseBody`
* Implementing MVC architecture with Thymeleaf
* Serving static resources
----

## Notes

* The application runs on port **8080** by default
* Static files must be placed in the `/static` directory
* Templates must be placed in the `/templates` directory

---
