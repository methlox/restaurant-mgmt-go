# Restaurant Management RESTful API
This is a RESTful API for managing a restaurant's operations, including customers, menu, orders, food, table, and invoice. It is built using the Gin framework for handling HTTP requests and MongoDB as the database.

## Features
- Customers: Manage customer information such as name, email, phone, and address.
- Menu: Add, update, and delete menu items for each restaurant, along with their details and pricing.
- Orders: Create, update, and delete orders for customers along with their details and pricing.
- Food: Create, update, and delete food for customers along with their details and pricing.
- Table: Create, update, and delete tables for customers for reservation.
- Invoice: Create, update, and delete invoice for customers along with their details and pricing.


## Prerequisites
- Go (1.16+)
- `github.com/gin-gonic/gin` (Gin framework)
- `github.com/dgrijalva/jwt-go` (JWT library)
- `github.com/joho/godotenv`

## Installation
### 1. Clone the repository
```gitbash
git clone https://github.com/methlox/restaurant-mgmt-go/
cd restaurant-mgmt-go
```

### 2. Install the required Go packages:
```bash
go get -u github.com/gin-gonic/gin
go get -u github.com/dgrijalva/jwt-go
go get -u github.com/joho/godotenv
go mod tidy
```

### 3. Run the application
```
go run main.go
```

## API Endpoints
The API provides endpoints to perform various operations on customers, menu, orders, food, table, and invoice.

### Users (Authentication)
- The User model represents a user (admin) of the restaurant.
- `GET /users`: Get all users
- `GET /users/{user_id}`: Get a specific user.
- `POST /auth/register`: Register a user
- `POST /auth/login`: Login a user and get a JWT token

### Menu
- `GET /menus`: Get all menu items for a restaurant.
- `GET /menus/{menu_id}`: Get a specific menu item.
- `POST /menus`: Add a new menu item to a restaurant.
- `PATCH /menus/{menu_id}`: Update a menu item.

### Orders
- `GET /orders`: Get all orders for a restaurant.
- `GET /orders/{order_id}`: Get a specific order.
- `POST /orders`: Add a new order to a restaurant.
- `PATCH /orders/{order_id}`: Update a order.

### Order Items
- `GET /orderItems`: Get all order items for a restaurant.
- `GET /orderItems/{orderItem_id}`: Get a specific order item.
- `GET /orderItems/{order_id}`: Get a specific order item of a order.
- `POST /orderItems`: Add a new order item.
- `PATCH /orderItems/{orderItem_id}`: Update a order item.

### Table
- `GET /tables`: Get all tables for a restaurant.
- `GET /tables/{table_id}`: Get a specific table.
- `POST /tables`: Add a new table to a restaurant.
- `PATCH /tables/{table_id}`: Update a table.

### Invoice
- `GET /invoices`: Get all invoices for a restaurant.
- `GET /invoices/{invoice_id}`: Get a specific invoice.
- `POST /invoices`: Add a new invoice to a restaurant.
- `PATCH /invoices/{invoice_id}`: Update an invoice.

## Authentication
The API supports authentication using JSON Web Tokens (JWT). To access protected endpoints, clients must include a valid JWT token in the Authorization header of their requests.

## Contributing
Contributions are welcome! Please follow the standard guidelines for contributing to open-source projects.

## License
This project is licensed under the MIT License. See the LICENSE file for details.

## Acknowledgements
Special thanks to Gin and Mongo DB for providing excellent tools to build this API.
