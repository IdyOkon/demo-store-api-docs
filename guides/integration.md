# How to Integrate the Demo Store API

This guide explains how to integrate the Demo Store API into an application.
It covers authentication, making requests, handling responses, and common errors.



## Prerequisites
- Basic understanding of REST APIs
- Familiarity with HTTP methods (GET, POST)
- An API client such as Postman or curl
- An API access token



## Base URL
All API requests are made to the following base URL:


> This is a demo API intended for testing and documentation purposes.



## Step 1: Authentication
The Demo Store API uses token-based authentication.

Include your API token in the `Authorization` header of every request:



## Step 2: Retrieve Products

GET /products

Example Response

{

  "products": [
  
    {
      "id": "p123",
      
      "name": "Wireless Headphones",
      
      "price": 120.00,
      
      "currency": "USD"
      
    }
  ]
}


## Step 3: Create an order

POST /orders

Request body

{
  "product_id": "p123",
  
  "quantity": 1
  }

Example response

{
  "order_id": "o456",
  
  "status": "created",
  
  "total": 120.00
  }


## Step 4: Error Handling

The API uses standard HTTP status codes:

 | Status Code	| Description
|------ | ---------- |
| 400	 | Bad request |
| 401  | Unauthorized |
| 404  | Resource not found |
| 500  | Internal server error |


## Common issues
- Missing or invalid authentication token
- Incorrect request payload format
- Invalid product or order IDs


## Conclusion
This guide demonstrated how to authenticate, retrieve products, and create orders using the Demo Store API.
For detailed endpoint specifications, refer to the main API documentation.

## Limitations
- Intended for demo and testing purposes only
- Data may reset without notice
- Not suitable for production use
