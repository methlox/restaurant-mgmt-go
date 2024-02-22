# Restaurant Management RESTful API
This is a RESTful API for managing a restaurant's operations, including customers, menu items, orders, food, table, and invoice. It is built using the Gin framework for handling HTTP requests and MongoDB as the database.

## Features
- Customers: Manage customer information such as name, email, phone, and address.
- Menu Items: Add, update, and delete menu items for each restaurant, along with their details and pricing.
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
The API provides endpoints to perform various operations on customers, restaurants, menu items, orders, delivery drivers, delivery information, and customer reviews. Refer to the [API documentation](api-documentation.md) for detailed information on each endpoint, request, and response formats.

## Authentication
The API supports authentication using JSON Web Tokens (JWT). To access protected endpoints, clients must include a valid JWT token in the Authorization header of their requests.

## Contributing
Contributions are welcome! Please follow the standard guidelines for contributing to open-source projects.

## License
This project is licensed under the MIT License. See the LICENSE file for details.

## Acknowledgements
Special thanks to Gin and Mongo DB for providing excellent tools to build this API.
