# Project Goals
- Create a react web application from scratch.
- Setting the project using babel and webpack. 
- Use CSS and SASS.
- Demonstrate the immutability of React
- A bit of react hooks
- Use typescript

## Babel
- It will transpile the modern javascript code for the browsers interpretators.
https://babeljs.io/docs/en/

**Add dependencies**
```
yarn add @babel/core @babel/cli @babel/preset-env -D              
```

- Create a babel.config.js
- Because of React use html inner of javascript we need to add another dependencie:
```
yarn add @babel/preset-react -D
```

## Webpack
- Allow us import several kind of files like css, hbs, sass and others, and transpile it for the browsers.

**Add dependencies**
```
yarn add webpack webpack-cli babel-loader -D
```

- Create the file webpack.config.js where will be all the settings to import modules.