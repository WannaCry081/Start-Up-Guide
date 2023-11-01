# JavaScript Environment Setup

## Frontend Configuration

### 📦 Frontend Packages Used

| Development Tools Used | | |
|------------------------|-|-|
| vite | @types/node | tailwindcss |
| postcss | autoprefixer | axios |
| framer-motion | react-redux | @reduxjs/toolkit | 
| formik | shadcn-ui@latest | Yup |

### 🛠 Frontend Environment Setup

Configure your frontend environment using a curated selection of packages. Simply follow the steps below:

1. Initialize your React Typescript project using Vite and then install tailwindcss:
```powershell
# Initialize Project Directory
$ npm create vite@latest frontend
$ cd frontend && npm i

# Install Tailwindcss
$ npm install -D tailwindcss postcss autoprefixer
$ npx tailwindcss init -p
```
2. Modify the `tailwind.config.js` file. Locate the `content` property and replace it with:
```js
// Configure tailwind.config.js to recognize 
// the following files extension
content: [
    "./index.html",
    "./src/**/*.{js,ts,jsx,tsx}",
]
```
3. Set up the styles:
   - Create a `styles` folder inside the `src` directory.
   - Inside the `styles` directory, create a `index.css` file and insert the following:
```css
/* To ensure css utilize tailwindcss styles */
@tailwind base;
@tailwind components;
@tailwind utilities;
```
4. Test your installation:
```powershell 
$ npm run dev
```
If tailwindcss styles are not reflecting, refer to the [official vite+tailwindcss setup guide](https://tailwindcss.com/docs/guides/vite).

4. Create a `jsconfig.json` then copy paste the contents of the code below

```json
{
    "baseUrl" : ".",
    "compilerOptions": {
        "paths": {
        "@/*": ["./src/*"]
        }
    }
}
```

6. Continue with the installation of other essential packages:
```powershell
# Install essential packages
$ npm i axios react-router-dom framer-motion react-redux @reduxjs/toolkit
$ npm i -D @types/node

# Install Shadcn-ui to your project
$ npx shadcn-ui@latest init
```

Follow these steps inorder to prevent any errors to occur
```powershell
$ Would you like to use TypeScript (recommended)? no
$ Which style would you like to use? › New York
$ Which color would you like to use as base color? › Zinc
$ Where is your global CSS file? › › src/styles/index.css
$ Do you want to use CSS variables for colors? › yes
$ Where is your tailwind.config.js located? › tailwind.config.js
$ Configure the import alias for components: › src/@/components
$ Configure the import alias for utils: › src/@/lib/utils
$ Are you using React Server Components? › no
```

After installing the necessary packages and `shadcn-ui`. Next is to configure the `vite.config.js`, just follow the instructions below

```JavaScript
// Update vite.config.js
resolve: {
    alias: [{
        find : "@Components",
        replacement : "/src/@/components"
    }, {
        find : "@Lib",
        replacement : "/src/@/lib"
    }],
},
```

Once you've completed the required steps, use the command below to launch your program. If no errors appear, congratulations on a successful setup!

```powershell
# To run the frontend program
$ npm run dev
```


### 📂 Frontend Folder and File Structure

```powershell
📂 frontend
│
├── 📂 node_modules
├── 📂 public 
├── 📂 src
│   ├── 📂 @
│   │   ├── 📂 components
│   │   └── 📂 lib
│   ├── 📂 assets
│   ├── 📂 layouts
│   ├── 📂 pages
│   ├── 📂 redux
│   ├── 📂 styles
│   │   └── 📄 index.css
│   ├── 📂 hooks
│   ├── 📄 App.jsx
│   └── 📄 main.jsx
│
├── 📄 .dockerignore
├── 📄 Dockerfile
├── 📄 package.json
├── 📄 tailwind.config.js
├── 📄 jsconfig.json
└── 📄 vite.config.js
```

---

## Backend Configuration

### 📦 Backend Packages Used

| Development Tools Used | | |
|------------------------|-|-|
| express | express-async-handler | mongoose |
| jsonwebtoken | cookie-parser | cors |
| bcryptjs | multer | dotenv | 
| nodemon | | |

### 🛠 Backend Project Setup

1. Initialize the backend directory and basic configurations:
```powershell
# Initialize Project Directory
$ mkdir backend && cd backend
$ npm init -y

# Create a src directory and main index.ts file
$ mkdir src && cd src && touch index.js
```
2. Update the contents of your `package.json`, copy and paste the command below to your `package.json`
```JavaScript
// Update Package.json
{
    "type": "module",
    "scripts": {
        "server" : "nodemon src/index.js"
    },
}
```

3. Install necessary packages:
```powershell
# Install a dev dependency `nodemon`
$ npm -D nodemon 

# Backend essential packages
$ npm i express express-async-handler dotenv cookie-parser jsonwebtoken bcryptjs mongoose cors multer 
```
4. Build and run the backend:
```powershell
# To run the backend program
$ npm run server
```

### 📂 Backend Folder and File Structure

```powershell
📂 backend
│
├── 📂 node_modules
├── 📂 src
│   ├── 📂 controllers
│   ├── 📂 routers
│   ├── 📂 middlewares
│   ├── 📂 config
│   ├── 📂 utils
│   ├── 📂 models
│   └── 📄 index.js
│
├── 📄 .dockerignore
├── 📄 Dockerfile
└── 📄 package.json
```

Happy Coding! ✨