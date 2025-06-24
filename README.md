Product API Documentation 

Overview - A simple CRUD API for managing product details, built using Express.js and connected to a MongoDB database via Mongoose.

The API supports - Adding a product, Viewing all products, Viewing a product by ID, Updating a product, and deleting a product by ID.

Base URL - http://localhost:3000/

Endpoints - a) GET - /api/products
Fetches all products in database
Response - 200 OK -> Returns an array of all products, 500 -> Internal server error on failure.

b) GET - /api/product/:id
Fetch a product by its ID
Response - 200 OK -> Returns the product object, 500 -> Internal server error on invalid or incorrect ID.

c) POST - /api/products
Create a new product (Can be added in JSON and formUrl encoded format as well, to be added inside the body).
Response - 200 OK -> Product created and displayed, 500 -> Internal server error or validation failure.

d) PUT - /api/product/:id
Update an existing product by ID
Response - 200 OK -> Updated product returned, 404 Not Found -> if product does not exist, 500 -> Internal server error.

e) DELETE - /api/product/:id
Delete a product by ID
Response - 200 OK -> Delete success message, 404 Not Found -> product not found, 500 -> Internal server error.

Data Model - Mongoose Schema
Each product document is automatically given - createdAt, updatedAt due to timestamps.

Status codes - 


Technologies used - Node.js, Express.js, MongoDB, Nodemon, Postman

Server - Server runs on localhost:3000 and to start use command npm run dev (dev linked in package.json as “nodemon index.js”).

Postman Collection - All endpoints of the API have been tested using Postman.
Collection link - https://gopal-2827773.postman.co/workspace/My-Workspace~75af8666-f0ad-488f-80da-2ccac54063ed/collection/45953821-df990992-d820-4b8c-9bdc-851c56f2e759?action=share&creator=45953821

Tested Endpoints - Create product (POST), Get all products (GET), Get product by ID (GET), Update product (PUT), Delete product (DELETE).
Each request includes - headers and body (wherever needed), response in JSON, and status codes upon execution.
