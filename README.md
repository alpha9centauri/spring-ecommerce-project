
# E-Commerce Spring Boot Application

### Overview

This e-commerce project is a full-featured web application built with **Spring Boot** and **Maven**. Designed to provide a scalable and robust foundation for e-commerce platforms, this application manages product listings, user accounts, orders, and payment processing. 

### Features

- **Product Management**: Add, edit, and remove products with detailed descriptions, pricing, and stock levels.
- **User Accounts**: Secure user registration, login, and account management.
- **Order Processing**: Cart functionality, order creation, and tracking.
- **Payment Gateway Integration**: Simplifies online payments.
- **Responsive and Scalable**: Designed to scale with Spring Boot’s robust architecture.

### Tech Stack

- **Backend**: Java, Spring Boot, Spring Data JPA
- **Build Tool**: Maven
- **Database**: Configurable in `application.properties` (e.g., MySQL, PostgreSQL)
- **Frontend**: Placeholder for potential integration with frameworks like Angular or React

### Getting Started

1. **Clone the Repository**:
   ```bash
   git clone <repository-url>
   cd spring-ecommerce-project
   ```

2. **Build and Run**:
   - Make sure Java and Maven are installed.
   - Use the Maven wrapper to package and run the application:

     ```bash
     ./mvnw spring-boot:run
     ```

3. **Access the Application**:
   - Open `http://localhost:8080` in your browser.

### Configuration

- **Database**: Configure database connection settings in `src/main/resources/application.properties`.
- **Environment Variables**: Set environment-specific variables for security and customization.

### Why This Project?

This e-commerce application demonstrates real-world skills in full-stack development, integrating Spring Boot with various enterprise-level components to create a fully-functional e-commerce platform.



## API Documentation

Below is a list of available APIs, organized by controller, HTTP method, and endpoint.

| HTTP Method | Path                                                       | Description                                       | Controller               |
|-------------|------------------------------------------------------------|---------------------------------------------------|--------------------------|
| **POST**    | `/addresses`                                               | Create a new address                              | AddressController.java    |
| **GET**     | `/addresses`                                               | Retrieve a list of all addresses                  | AddressController.java    |
| **GET**     | `/addresses/{addressId}`                                   | Retrieve a specific address by ID                 | AddressController.java    |
| **GET**     | `/users/addresses`                                         | Retrieve all addresses for a specific user        | AddressController.java    |
| **PUT**     | `/addresses/{addressId}`                                   | Update an existing address                        | AddressController.java    |
| **DELETE**  | `/addresses/{addressId}`                                   | Delete an address by ID                           | AddressController.java    |
| **POST**    | `/signin`                                                  | Sign in a user                                    | AuthController.java       |
| **POST**    | `/signup`                                                  | Register a new user                               | AuthController.java       |
| **GET**     | `/username`                                                | Retrieve the username of the current user         | AuthController.java       |
| **GET**     | `/user`                                                    | Retrieve the details of the current user          | AuthController.java       |
| **POST**    | `/signout`                                                 | Sign out the current user                         | AuthController.java       |
| **POST**    | `/carts/products/{productId}/quantity/{quantity}`          | Add a product to the cart with specified quantity | CartController.java       |
| **GET**     | `/carts`                                                   | Retrieve all carts                                | CartController.java       |
| **GET**     | `/carts/users/cart`                                        | Retrieve the cart of a specific user              | CartController.java       |
| **PUT**     | `/cart/products/{productId}/quantity/{operation}`          | Update product quantity in the cart               | CartController.java       |
| **DELETE**  | `/carts/{cartId}/product/{productId}`                      | Remove a product from the cart                    | CartController.java       |
| **GET**     | `/public/categories`                                       | Retrieve a list of all categories                 | CategoryController.java   |
| **POST**    | `/public/categories`                                       | Create a new category                             | CategoryController.java   |
| **DELETE**  | `/admin/categories/{categoryId}`                           | Delete a category by ID                           | CategoryController.java   |
| **PUT**     | `/public/categories/{categoryId}`                          | Update an existing category                       | CategoryController.java   |
| **POST**    | `/order/users/payments/{paymentMethod}`                    | Create a new order with the specified payment     | OrderController.java      |
| **POST**    | `/admin/categories/{categoryId}/product`                   | Add a product to a category                       | ProductController.java    |
| **GET**     | `/public/products`                                         | Retrieve all products                             | ProductController.java    |
| **GET**     | `/public/categories/{categoryId}/products`                 | Retrieve products by category                     | ProductController.java    |
| **GET**     | `/public/products/keyword/{keyword}`                       | Search products by keyword                        | ProductController.java    |
| **PUT**     | `/admin/products/{productId}`                              | Update product details                            | ProductController.java    |
| **DELETE**  | `/admin/products/{productId}`                              | Delete a product by ID                            | ProductController.java    |
| **PUT**     | `/products/{productId}/image`                              | Update product image                              | ProductController.java    |

