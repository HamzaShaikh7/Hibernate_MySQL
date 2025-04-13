# Hibernate_MySQL


# 📦 Project Dependencies

├── **Spring Web** - For building web applications with Spring MVC  
├── **MySQL Driver** - JDBC driver for MySQL database connectivity  
├── **Spring Data JPA** - Persist data in SQL stores using JPA  
├── **Spring Boot DevTools** - Provides developer tools and auto-restart  
└── **Lombok** - Reduces boilerplate code via annotations


# 📁 Project Structure

**src/**<br>
└── **main/**<br>
............  ├── **java/com/connect/Spring_Boot_MySQL_Hibernate/**<br>
............  │ ............  ├── controller/ProductController.java<br>
............  │ ............  ├── entity/Product.java<br>
............  │ ............  ├── repository/ProductRepository.java<br>
............  │ ............  ├── service/ProductService.java<br>
............  │ ............  └── SpringBootMySqlHibernateApplication.java<br>
............  └── **resources/**<br>
.......................    └── application.properties<br>






Create a product:
-----------------
POST http://localhost:8080/products/add

    Body (JSON):
    {
        "name": "Laptop",
        "price": 999.99,
        "quantity": 10
    }


Get all products:
-----------------
GET http://localhost:8080/products



Get product by ID:
------------------
GET http://localhost:8080/products/1


Get product by Name:
------------------
GET http://localhost:8080/products/name/laptop



Update product:
---------------
PUT http://localhost:8080/products/update

    Body (JSON):
    {
        "id": 1,
        "name": "Updated Laptop",
        "price": 1099.99,
        "quantity": 5
    }


Delete product by ID:
---------------
DELETE http://localhost:8080/products/delete/1


Find products by price range:
-----------------------------
GET http://localhost:8080/products/price-range?minPrice-100&maxPrice-500


Find products with low stock:
-----------------------------
GET http://localhost:8080/products/low-stock?maxQuantity-5

