# Product Inventory MERN App

This workspace contains a simple Product Inventory Management System built with the MERN stack to demonstrate CRUD operations.

Folders:
- `server/` - Express + Mongoose backend
- `client/` - React (Vite) frontend

Server
------

1. Create a `.env` file inside the `server` folder (optional). You can set:

```
MONGODB_URI=mongodb://127.0.0.1:27017/product_inventory
PORT=5000
```

If you don't provide `MONGODB_URI`, the server will attempt to connect to `mongodb://127.0.0.1:27017/product_inventory`.

2. Install dependencies and start dev server (from project root or inside `server`):

```powershell
cd server; npm install
npm run dev    # starts nodemon server.js
```

Available endpoints (base `http://localhost:5000`):
- POST `/api/addproduct` - create product (JSON body: { name, price, quantity })
- GET `/getAllproducts` - fetch all products
- PUT `/editproduct/:id` - update product by id (JSON body: fields to update)
- DELETE `/deleteproduct/:id` - delete product by id

Client
------

1. Install and start the frontend (in a new terminal):

```powershell
cd client; npm install
npm run dev
```

2. Open `http://localhost:5173` in your browser.

Usage
-----

- Use the Product List page to view, edit, or delete items.
- Use Add Product to create new products.

Notes
-----

- Ensure MongoDB is running (locally or provide a remote URI in `.env`).
- The server logs connection status on startup.


License
-------
MIT
