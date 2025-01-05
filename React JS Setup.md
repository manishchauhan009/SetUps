

To set up a React.js environment, follow these steps:

---

### **1. Prerequisites**
Before you start, ensure you have the following installed:
- **Node.js and npm** (Node Package Manager):
  - Download and install from [Node.js official website](https://nodejs.org/). 
  - Verify installation by running:
    ```bash
    node -v
    npm -v
    ```

- **Code Editor**:
  - Use a code editor like [Visual Studio Code (VS Code)](https://code.visualstudio.com/).

---

### **2. Create a New React App**
React offers a tool called **Create React App (CRA)** for a quick setup.

#### Using `npx` (recommended):
1. Open a terminal.
2. Run the following command:
   ```bash
   npx create-react-app my-app
   ```
   Replace `my-app` with your desired project name.

3. Navigate to your project directory:
   ```bash
   cd my-app
   ```

4. Start the development server:
   ```bash
   npm start
   ```
   This opens a development server at `http://localhost:3000`.

---

### **3. Project Structure**
Once CRA completes, the folder structure will look like this:

```
my-app
├── node_modules
├── public
├── src
│   ├── App.css
│   ├── App.js
│   ├── index.css
│   ├── index.js
├── .gitignore
├── package.json
├── README.md
└── yarn.lock
```

### **4. Key Commands**
- **Run Development Server**:
  ```bash
  npm start
  ```
- **Build for Production**:
  ```bash
  npm run build
  ```
- **Test Application**:
  ```bash
  npm test
  ```
- **Install Additional Packages**:
  ```bash
  npm install <package-name>
  ```

---

### **5. Customizing the App**
Start editing the `src/App.js` file to make changes to your app. You can add components and styles as needed.

---

### **6. Optional Tools and Enhancements**
- **React Developer Tools**:
  - Install the React DevTools browser extension for debugging.
- **ESLint and Prettier**:
  - For code linting and formatting:
    ```bash
    npm install eslint prettier --save-dev
    ```
