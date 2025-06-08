# Express.js Assignment

This project is an Express.js server for Week 2 of the MERN Stack course.

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) installed

### Installation

```bash
git clone https://github.com/your-username/week-2-express-js-assignment-DOMOSH85.git
cd week-2-express-js-assignment-DOMOSH85
npm install
```

### Running the Server

```bash
npm start
```
The server will start on [http://localhost:3000](http://localhost:3000) by default.

---

## API Documentation

### Base URL

```
http://localhost:3000
```

### Endpoints

#### 1. `GET /api/items`

- **Description:** Retrieve all items.
- **Response:**
   ```json
   [
     {
      "id": 1,
      "name": "Item 1"
     },
     {
      "id": 2,
      "name": "Item 2"
     }
   ]
   ```

#### 2. `GET /api/items/:id`

- **Description:** Retrieve a single item by ID.
- **Response:**
   ```json
   {
     "id": 1,
     "name": "Item 1"
   }
   ```

#### 3. `POST /api/items`

- **Description:** Create a new item.
- **Request Body:**
   ```json
   {
     "name": "New Item"
   }
   ```
- **Response:**
   ```json
   {
     "id": 3,
     "name": "New Item"
   }
   ```

#### 4. `PUT /api/items/:id`

- **Description:** Update an existing item.
- **Request Body:**
   ```json
   {
     "name": "Updated Item"
   }
   ```
- **Response:**
   ```json
   {
     "id": 1,
     "name": "Updated Item"
   }
   ```

#### 5. `DELETE /api/items/:id`

- **Description:** Delete an item by ID.
- **Response:**
   ```json
   {
     "message": "Item deleted"
   }
   ```

---

## Example Requests

### Using `curl`

**Get all items:**
```bash
curl http://localhost:3000/api/items
```

**Create an item:**
```bash
curl -X POST -H "Content-Type: application/json" -d '{"name":"Sample"}' http://localhost:3000/api/items
```

**Update an item:**
```bash
curl -X PUT -H "Content-Type: application/json" -d '{"name":"Updated"}' http://localhost:3000/api/items/1
```

**Delete an item:**
```bash
curl -X DELETE http://localhost:3000/api/items/1
```

---

## License

MIT