## Replication

### 1. Setup directory for project
```
mkdir react-boilerplate && cd $_
```

### 2. Installation

```
npx create-react-app ./ && 
npm install tailwindcss postcss-cli autoprefixer --save-dev && 
npm install eslint-plugin-react-hooks --save-dev && 
npm audit fix && npx tailwind init && touch postcss.config.js && 
mkdir -p ./src/styles && 
touch ./src/styles/tailwind.css && 
rm src/App.test.js src/App.css src/index.css src/logo.svg src/serviceWorker.js &&
echo -e "@tailwind base;\n@tailwind components;\n@tailwind utilities;" > ./src/styles/tailwind.css &&
echo -e "module.exports = {" > ./postcss.config.js &&
echo -e  "  plugins: [require('tailwindcss'), require('autoprefixer')]" >> ./postcss.config.js &&
echo -e "};" >> ./postcss.config.js &&
echo -e "import React from 'react'\n\nexport default function App() {" > ./src/App.js &&
echo -e "  return (" >> ./src/App.js &&
echo -e "    <div className='text-4xl font-bold text-center text-blue-500'>" >> ./src/App.js &&
echo -e "      Hello World" >> ./src/App.js &&
echo -e "    </div>\n  );\n}" >> ./src/App.js &&
echo -e "import React from 'react'" > ./src/index.js &&
echo -e "import ReactDOM from 'react-dom'" >> ./src/index.js &&
echo -e "import './styles.css'" >> ./src/index.js &&
echo -e "import App from './App'\n" >> ./src/index.js &&
echo -e "ReactDOM.render(<App />, document.getElementById('root'));" >> ./src/index.js 
```

### 3. Additional Code to Files

#### package.json:

```
  "scripts": {
    "start": "react-scripts start",
    "build": "react-scripts build",
    "test": "react-scripts test",
    "eject": "react-scripts eject",
    "build:styles": "postcss src/styles/tailwind.css -o src/styles.css",
    "prebuild": "npm run build:styles",
    "prestart": "npm run build:styles"
  },
```

---

## Archive

#### src/styles/Tailwind.css
```
echo -e "@tailwind base;\n@tailwind components;\n@tailwind utilities;" > ./src/styles/tailwind.css
```

```
echo -e "module.exports = {" > ./postcss.config.js &&
echo -e  "  plugins: [require('tailwindcss'), require('autoprefixer')]" >> ./postcss.config.js &&
echo -e "};" >> ./postcss.config.js
```

#### src/App.js
This boilerplate is copied with the bash commands.
```
import React from "react";

function App() {
  return (
    <div className="text-4xl font-bold text-center text-blue-500">
      Hello World!
    </div>
  );
}

export default App;
```
```
echo -e "import React from 'react'\n\nexport default function App() {" > ./src/App.js &&
echo -e "  return (" >> ./src/App.js &&
echo -e "    <div className='text-4xl font-bold text-center text-blue-500'>" >> ./src/App.js &&
echo -e "      Hello World" >> ./src/App.js &&
echo -e "    </div>\n  );\n}" >> ./src/App.js
```

#### src/index.js

```
import React from "react";
import ReactDOM from "react-dom";
import "./styles.css";
import App from "./App";

ReactDOM.render(<App />, document.getElementById("root"));
```
```
echo -e "import React from 'react'" > ./src/index.js &&
echo -e "import ReactDOM from 'react-dom'" >> ./src/index.js &&
echo -e "import './styles.css'" >> ./src/index.js &&
echo -e "import App from './App'\n" >> ./src/index.js &&
echo -e "ReactDOM.render(<App />, document.getElementById('root'));" >> ./src/index.js 
```
---

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `yarn start`

Runs the app in the development mode.<br />
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.<br />
You will also see any lint errors in the console.

### `yarn test`

Launches the test runner in the interactive watch mode.<br />
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `yarn build`

Builds the app for production to the `build` folder.<br />
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.<br />
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `yarn eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (Webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: https://facebook.github.io/create-react-app/docs/code-splitting

### Analyzing the Bundle Size

This section has moved here: https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size

### Making a Progressive Web App

This section has moved here: https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app

### Advanced Configuration

This section has moved here: https://facebook.github.io/create-react-app/docs/advanced-configuration

### Deployment

This section has moved here: https://facebook.github.io/create-react-app/docs/deployment

### `yarn build` fails to minify

This section has moved here: https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify
