# Backend-Nodejs
Built REST API's using Nodejs , Expressjs and a NOSQL-database for managing the data 

# Restaurant Vendor API Documentation

This documentation provides information on the available API endpoints for managing restaurant vendors and their products. Below are the endpoints and their descriptions:

## Vendor Endpoints

### Get Vendor Details
**Endpoint:** `https://backend-nodejs-restaurent-register-apis.onrender.com/vendor/getDetails`

**Description:** Retrieves the details of all registered vendors.

**Method:** GET

**Example Request:**
```bash
curl -X GET https://backend-nodejs-restaurent-register-apis.onrender.com/vendor/getDetails
```

### Get Single Vendor by ID
**Endpoint:** `https://backend-nodejs-restaurent-register-apis.onrender.com/vendor/singleVendor/{vendorId}`

**Description:** Retrieves the details of a single vendor based on the vendor ID.

**Method:** GET

**Parameters:**
- `vendorId`: The ID of the vendor.

**Example Request:**
```bash
curl -X GET https://backend-nodejs-restaurent-register-apis.onrender.com/vendor/singleVendor/6649730b78c6eca02b492e81
```

## Product Endpoints

### Get Firm Added Products
**Endpoint:** `https://backend-nodejs-restaurent-register-apis.onrender.com/product/firmProducts/{firmId}`

**Description:** Retrieves the products added by a firm/restaurant based on the firm ID.

**Method:** GET

**Parameters:**
- `firmId`: The ID of the firm/restaurant.

**Example Request:**
```bash
curl -X GET https://backend-nodejs-restaurent-register-apis.onrender.com/product/firmProducts/6649737478c6eca02b492e86
```

## Image Endpoint

### Get Product Image
**Endpoint:** `https://backend-nodejs-restaurent-register-apis.onrender.com/uploads/{imageName}`

**Description:** Retrieves the image of a product based on the image name.

**Method:** GET

**Parameters:**
- `imageName`: The name of the image file.

**Example Request:**
```bash
curl -X GET https://backend-nodejs-restaurent-register-apis.onrender.com/uploads/1716103446359.jpeg
```

## Summary of Endpoints

| Endpoint                                                     | Method | Description                                           |
|--------------------------------------------------------------|--------|-------------------------------------------------------|
| `/vendor/getDetails`                                         | GET    | Retrieves details of all vendors                      |
| `/vendor/singleVendor/{vendorId}`                            | GET    | Retrieves details of a single vendor by vendor ID     |
| `/product/firmProducts/{firmId}`                             | GET    | Retrieves products added by a firm by firm ID         |
| `/uploads/{imageName}`                                       | GET    | Retrieves product image by image name                 |

This README file provides a comprehensive guide to the available API endpoints for managing restaurant vendor details and their products, along with the product images. Use the example requests provided to interact with the API.
