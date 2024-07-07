# Tailwind CSS Setup with Vite

Follow these steps to set up Tailwind CSS in your project using Vite.

## Steps

1. **Initialize a new Node.js project**

   Open your terminal and run:
   ```bash
   npm init -y
2. **Install Tailwind CSS, PostCSS, and Autoprefixer**
   Open your terminal and run:
   ```bash
   npm install -D tailwindcss postcss autoprefixer
3. **Generate Tailwind and PostCSS configuration files**  
  Open your terminal and run:
   ```bash
   npx tailwindcss init -p

4. **Configure Tailwind**
    Open the tailwind.config.js file and set the content property:
    ```javascript
    module.exports = {
    content: ["*"],
    theme: {
    extend: {},
    },
    plugins: [],
    };

5. **Create your input CSS file**
  Create a file named input.css in your project directory and add the following lines:
  ```css
    @tailwind base;
    @tailwind components;
    @tailwind utilities;
```

6. **Install Vite**
  ```terminal
  npm install vite
```

7. **Update package.json scripts**
    Open package.json and add the following script:
    ```json
    "scripts": {
  "start": "vite"
}


8. **Link your CSS file in your HTML**
  Ensure your HTML file links to the input.css file you created:
    ```html
<link href="/path/to/input.css" rel="stylesheet">

9. **Start the development server**
  Run the following command to start Vite:
  ```bash
npm run start

