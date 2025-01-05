To set up **Node.js** and **Express**, follow these steps:

---

### **1. Prerequisites**
Ensure you have the following:
- **Node.js**: Install it from the [Node.js website](https://nodejs.org/).
  - Verify installation:
    ```bash
    node -v
    npm -v
    ```

- **Code Editor**: Use one like [Visual Studio Code (VS Code)](https://code.visualstudio.com/).

---

### **2. Create a New Project**

1. **Initialize a Node.js Project**:
   - Open a terminal and create a new folder for your project:
     ```bash
     mkdir my-express-app
     cd my-express-app
     ```
   - Initialize a `package.json` file:
     ```bash
     npm init -y
     ```

   This will generate a `package.json` file with default values.

---

### **3. Install Express**
Install the Express package using npm:
```bash
npm install express
```

---

### **4. Create Your Server File**
1. Create a new file named `index.js` in the project folder:
   ```bash
   touch index.js
   ```
2. Add the following basic Express server code to `index.js`:
   ```javascript
   const express = require('express');
   const app = express();
   const PORT = 3000;

   // Define a route
   app.get('/', (req, res) => {
       res.send('Hello, Express!');
   });

   // Start the server
   app.listen(PORT, () => {
       console.log(`Server is running on http://localhost:${PORT}`);
   });
   ```

---

### **5. Run the Server**
Run the server using Node.js:
```bash
node index.js
```
Open your browser and go to [http://localhost:3000](http://localhost:3000) to see the message: `Hello, Express!`.

---

### **6. Folder Structure**
Your project folder should now look like this:
```
my-express-app
├── node_modules
├── package.json
├── package-lock.json
└── index.js
```

---

### **7. Adding Middleware**
Express supports middleware to handle requests. For example:
```javascript
// Middleware to parse JSON
app.use(express.json());

// Middleware to log requests
app.use((req, res, next) => {
    console.log(`${req.method} ${req.url}`);
    next();
});
```

---

### **8. Install Nodemon for Development (Optional)**
To automatically restart the server on file changes, use `nodemon`:
1. Install globally:
   ```bash
   npm install -g nodemon
   ```
2. Start the server with `nodemon`:
   ```bash
   nodemon index.js
   ```

---

### **9. Additional Packages for Express Apps**
You may need additional libraries based on your requirements:
- **Body parsing** (if using older Express versions):
  ```bash
  npm install body-parser
  ```
- **CORS** (for cross-origin requests):
  ```bash
  npm install cors
  ```
