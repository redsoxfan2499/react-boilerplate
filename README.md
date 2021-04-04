# react-boilerplate

##### create brand new folder with name of project  example  react-project
inside of here create a folder called  src
inside here create file called index.html   and styles.css   and App.js file  all inside src folder

    included your style.css with normal html markup
   create a div as such
   `<div id="root">Not rendered</div>`
    and
    `<script src="App.js"></script>`
   inside body

```javascript
npm init -y 
```

##### next install Prettier  
```javascript
npm install -D prettier
```
next add a prettier script in package.json file
```javascript
"format": "prettier \"src/**/*.{js,html}\" --write",
```

create a Prettier config file   .prettierrc
 inside file use the defaults  by placing  empty brackets
 ```javascript
 {}
 ```
 
 next install eslint and eslint for prettier
 ```javascript
 npm install -D eslint eslint-config-prettier
 ```

 now create eslint config file titled
 `.eslintrc.json`
 inside of file place this:
 ```javascript
 {
    "extends": [ 
        "eslint:recommended",
        "plugin:import/errors",
        "plugin:react/recommended",
        "plugin:jsx-a11y/recommended",
        "prettier" 
    ],
    "rules": {
        "react/prop-types": 0,
        "no-console": 1,
        "react-hooks/rules-of-hooks": 2,
        "react-hooks/exhaustive-deps": 1
    },
    "plugins": ["react", "import", "jsx-a11y", "react-hooks"],
    "parserOptions": {
        "emcaVersion": 2018,
        "sourceType": "module",
        "ecmaFeatures": {
            "jsx": true
        }
    },
    "env": {
        "es6": true,
        "browser": true,
        "node": true
    },
    "settings": {
        "react": {
            "version": "detect"
        }
    }
}
```

now add script to package.json for eslint
```javascript
 "lint": "eslint \"src/**/*.{js,jsx}\"",
 ```
 
add .gitignore file
inside place the following
```javascript
node_modules
.DS_Store
.cache/
dist/
coverage/
.vscode/
.env
```

now install the Powerful Parcel
```javascript
npm install -D parcel-bundler
```

now add another script to package.json file
```javascript
"dev": "parcel src/index.html",
 ```

now install react react-dom
```javascript
npm install react react-dom```
