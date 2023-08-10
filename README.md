# Sale Campaign Management System API Documentation

Welcome to the API documentation for the Sale Campaign Management System. This documentation provides comprehensive details about the available APIs, their endpoints, request formats, and response structures.

## Accessing API Endpoints

You can access the various API endpoints provided by the Sale Campaign Management System through Swagger UI. Please use the following URL in your web browser to explore and interact with the APIs:

[Access Swagger UI](http://localhost:8888/swagger-ui/index.html#/)

## Product Controller

### Add Product

Add a new product to the catalog.

- **Endpoint**: `POST /products/add-product`
- **Request Body**:
  ```json
  {
    "id": "P123",
    "title": "Smartphone",
    "description": "High-end smartphone with advanced features.",
    "mrp": 25000.0,
    "currentPrice": 19999.0,
    "discount": 20.0,
    "inventory": 100
  }
  ```
- **Response**: HTTP Status 201 Created

### Get All Products

Retrieve a list of all products.

- **Endpoint**: `GET /products`
- **Response Example**:
  ```json
  [
    {
      "id": "P123",
      "title": "Smartphone",
      "description": "High-end smartphone with advanced features.",
      "mrp": 25000,
      "currentPrice": 19999,
      "discount": 20,
      "inventory": 100
    }
    // More product entries...
  ]
  ```

### Get Product by ID

Retrieve product details by ID.

- **Endpoint**: `GET /products/{product-id}`
- **Response Example**:
  ```json
  [
    {
      "id": "qwe1",
      "productId": "P123",
      "discount": 1000
    }
  ]
  ```

## Campaign Controller

### Add Campaign

Create a new sale campaign.

- **Endpoint**: `POST /campaigns/add-campaign`
- **Request Body**:
  ```json
  {
    "startDate": "2023-08-10",
    "endDate": "2023-08-15",
    "title": "Freedom Sale"
  }
  ```
- **Response**: HTTP Status 201 Created

### Get All Campaigns

Retrieve a list of all campaigns.

- **Endpoint**: `GET /campaigns`
- **Response Example**:
  ```json
  [
    {
      "id": 1,
      "startDate": "2023-08-10",
      "endDate": "2023-08-15",
      "title": "Freedom Sale",
      "campaignDiscounts": []
    }
    // More campaign entries...
  ]
  ```

## Campaign Discount Controller

### Add Campaign Discount

Add a discount to a campaign.

- **Endpoint**: `POST /campaign-discounts/add-campaign-discount`
- **Request Body**:
  ```json
  {
    "id": "qwe1",
    "campaignId": 1,
    "productId": "P123",
    "discount": 1000
  }
  ```
- **Response**: HTTP Status 201 Created

## Team 

👤 [Shimbhu Kumawat](https://github.com/Shimbhu77)
     

