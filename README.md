# Backend-Nodejs
Built REST API's using Nodejs, Expressjs, and a NoSQL database for managing the data.

# Restaurant Vendor API Documentation

This documentation provides information on the available API endpoints for managing restaurant vendors and their products. Below are the endpoints and their descriptions:

## Vendor Endpoints

### Vendor Registration
**Endpoint:** [`https://backend-nodejs-restaurent-register-apis.onrender.com/vendor/register`](https://backend-nodejs-restaurent-register-apis.onrender.com/vendor/register)

**Description:** Registers a new vendor.

**Method:** POST

**Request Body:**
- `userName`: Name of the vendor (string)
- `email`: Email address of the vendor (string)
- `password`: Password for the vendor (string)

### Vendor Login
**Endpoint:** [`https://backend-nodejs-restaurent-register-apis.onrender.com/vendor/login`](https://backend-nodejs-restaurent-register-apis.onrender.com/vendor/login)

**Description:** Authenticates a vendor and returns a JWT token.

**Method:** POST

**Request Body:**
- `email`: Email address of the vendor (string)
- `password`: Password for the vendor (string)

**Response:**
- `token`: JWT token for authenticated requests (string)

### Get Vendor Details
**Endpoint:** [`https://backend-nodejs-restaurent-register-apis.onrender.com/vendor/getDetails`](https://backend-nodejs-restaurent-register-apis.onrender.com/vendor/getDetails)

**Description:** Retrieves the details of all registered vendors.

**Method:** GET

**Headers:**
- `Authorization`: Bearer <JWT token>

### Get Single Vendor by ID
**Endpoint:** [`https://backend-nodejs-restaurent-register-apis.onrender.com/vendor/singleVendor/{vendorId}`](https://backend-nodejs-restaurent-register-apis.onrender.com/vendor/singleVendor/{vendorId})

**Description:** Retrieves the details of a single vendor based on the vendor ID.

**Method:** GET

**Parameters:**
- `vendorId`: The ID of the vendor.

**Headers:**
- `Authorization`: Bearer <JWT token>

## Product Endpoints

### Get Firm Added Products
**Endpoint:** [`https://backend-nodejs-restaurent-register-apis.onrender.com/product/firmProducts/{firmId}`](https://backend-nodejs-restaurent-register-apis.onrender.com/product/firmProducts/{firmId})

**Description:** Retrieves the products added by a firm/restaurant based on the firm ID.

**Method:** GET

**Parameters:**
- `firmId`: The ID of the firm/restaurant.

**Headers:**
- `Authorization`: Bearer <JWT token>

## Image Endpoint

### Get Product Image
**Endpoint:** [`https://backend-nodejs-restaurent-register-apis.onrender.com/uploads/{imageName}`](https://backend-nodejs-restaurent-register-apis.onrender.com/uploads/{imageName})

**Description:** Retrieves the image of a product based on the image name.

**Method:** GET

**Parameters:**
- `imageName`: The name of the image file.

## Summary of Endpoints

| Endpoint                                                                 | Method | Description                                           | Headers                 |
|--------------------------------------------------------------------------|--------|-------------------------------------------------------|-------------------------|
| [`/vendor/register`](https://backend-nodejs-restaurent-register-apis.onrender.com/vendor/register)                 | POST   | Registers a new vendor                                |                         |
| [`/vendor/login`](https://backend-nodejs-restaurent-register-apis.onrender.com/vendor/login)                       | POST   | Authenticates a vendor and returns a JWT token        |                         |
| [`/vendor/getDetails`](https://backend-nodejs-restaurent-register-apis.onrender.com/vendor/getDetails)             | GET    | Retrieves details of all vendors                      | Authorization: Bearer <JWT token> |
| [`/vendor/singleVendor/{vendorId}`](https://backend-nodejs-restaurent-register-apis.onrender.com/vendor/singleVendor/{vendorId}) | GET    | Retrieves details of a single vendor by vendor ID     | Authorization: Bearer <JWT token> |
| [`/product/firmProducts/{firmId}`](https://backend-nodejs-restaurent-register-apis.onrender.com/product/firmProducts/{firmId}) | GET    | Retrieves products added by a firm by firm ID         | Authorization: Bearer <JWT token> |
| [`/uploads/{imageName}`](https://backend-nodejs-restaurent-register-apis.onrender.com/uploads/{imageName})         | GET    | Retrieves product image by image name                 |                         |

This README file provides a comprehensive guide to the available API endpoints for managing restaurant vendor details and their products, along with the product images. Use the example requests provided to interact with the API. Note that some endpoints require a JWT token for authentication.
