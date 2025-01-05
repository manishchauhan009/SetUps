To set up **MongoDB**, follow these steps:

---

### **1. Install MongoDB**

1. **Download MongoDB**:
   - Visit the [MongoDB Download Center](https://www.mongodb.com/try/download/community).
   - Select your operating system and download the installer for the Community Edition.

2. **Install MongoDB**:
   - Follow the instructions in the installer.
   - During installation, ensure the **MongoDB Server** and **MongoDB Compass** options are selected.

3. **Verify Installation**:
   - After installation, open a terminal and run:
     ```bash
     mongo --version
     ```
   - If you see the version number, MongoDB is installed successfully.

---

### **2. Start MongoDB**

- **Start MongoDB Server**:
  - On most systems, MongoDB can be started as a service:
    ```bash
    mongod
    ```
  - Alternatively, if you installed MongoDB as a standalone binary, navigate to the installation folder and run the `mongod` executable.

- **Check if MongoDB is Running**:
  - Open another terminal and run:
    ```bash
    mongo
    ```
  - This should open the MongoDB shell.

---

### **3. Create a Database**
1. In the MongoDB shell, create a new database:
   ```javascript
   use myDatabase
   ```
2. Insert a sample record:
   ```javascript
   db.myCollection.insertOne({ name: "John Doe", age: 30, city: "New York" });
   ```
3. Query the collection:
   ```javascript
   db.myCollection.find();
   ```

---

### **4. Integrate MongoDB with Node.js**

1. **Install MongoDB Driver**:
   Run this command in your Node.js project:
   ```bash
   npm install mongodb
   ```

2. **Write a Sample Connection Script**:
   Create a file (e.g., `db.js`) and add:
   ```javascript
   const { MongoClient } = require('mongodb');

   const uri = 'mongodb://localhost:27017';
   const client = new MongoClient(uri);

   async function run() {
       try {
           await client.connect();
           console.log('Connected to MongoDB');

           const database = client.db('myDatabase');
           const collection = database.collection('myCollection');

           // Insert a document
           const doc = { name: "Jane Doe", age: 25, city: "San Francisco" };
           await collection.insertOne(doc);

           // Query documents
           const results = await collection.find({}).toArray();
           console.log('Documents:', results);
       } finally {
           await client.close();
       }
   }

   run().catch(console.error);
   ```

3. **Run the Script**:
   Execute the script using:
   ```bash
   node db.js
   ```

---

### **5. Install and Use GUI Tools**
You can use MongoDB Compass for a graphical interface:
- Open MongoDB Compass.
- Connect to your MongoDB instance (usually `mongodb://localhost:27017`).
- View and manage your databases and collections.

---

### Common Commands in MongoDB

| Command                           | Description                        |
|-----------------------------------|------------------------------------|
| `show dbs`                        | List all databases                |
| `use <db_name>`                   | Switch to a database              |
| `db.createCollection('name')`     | Create a new collection            |
| `db.collection.insertOne({...})`  | Insert a single document          |
| `db.collection.find()`            | Retrieve documents from a collection |
| `db.collection.deleteOne({...})`  | Delete a single document          |
| `db.collection.updateOne({...})`  | Update a single document          |

---

