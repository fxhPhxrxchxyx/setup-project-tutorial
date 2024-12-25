## Setup Project 🛠️
### 1. Update Website Name
Go to index.html in the root folder.
Update the <title> tag to iot workshop 2025.
Evaluation: Open the website in Chrome and capture a screenshot showing the updated title.

### 2. Clean Unused Files
Step 1: Go to src/App.css:

Delete all existing CSS.
Add the following global CSS:
```
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  border: "none";
}
```
Delete index.css and remove its import from main.tsx.


### Step 2: Go to src/App.tsx:

Remove all imports except import "./App.css";.
Update the file to:
```
import "./App.css";

function App() {
  return <></>;
}

export default App;
```

### 3. Create Folder Structure
Inside `src`  create the following folders:
- `pages`: For each page of the website.
- `components`: For reusable UI elements.
- `services`: For API calls (create api.ts inside this folder).
- `types`: For TypeScript types (create index.ts inside this folder).

Folder Structure Example:
```
src/
├── assets/
├── components/
├── pages/
├── services/
│   ├── api.ts
├── types/
│   ├── index.ts
```
### 4. Naming Conventions
Files in pages/ and components/ must start with an uppercase letter (e.g., Home.tsx).
For component-specific CSS, use .module.css (e.g., Button.module.css for Button.tsx).
Evaluation: Create a file Home.tsx in pages/ with the following content:

```
const Home = () => {
  return <div>This is Home page</div>;
};

export default Home;
```
### 5. Add Routing
Install react-router-dom:

`npm i react-router-dom`

Update App.tsx to include routing:
```
import "./App.css";
import { BrowserRouter, Routes, Route } from "react-router-dom";
import Home from "./pages/Home";

function App() {
  return (
    <>
      <BrowserRouter>
        <Routes>
          <Route path="/" element={<Home />}></Route>
        </Routes>
      </BrowserRouter>
    </>
  );
}

export default App;
```

## Common Errors
Cannot Import Component:
Ensure the file name starts with an uppercase letter (e.g., Home.tsx).
Routing Not Working:
Ensure react-router-dom is installed and properly imported.

Folder Structure
```
frontend/
├── public/
├── src/
│   ├── assets/
│   ├── components/
│   ├── hooks/
│   ├── pages/
│   ├── services/
│   │   ├── api.ts
│   ├── types/
│   │   ├── index.ts
│   ├── App.tsx
│   ├── index.tsx
│   ├── react-app-env.d.ts
│   ├── reportWebVitals.ts
│   ├── setupTests.ts
├── .prettierrc
├── tsconfig.json
└── package.json
```
