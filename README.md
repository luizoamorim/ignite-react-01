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
- Because of React use html inner of javascript we need to add another dependency:
```
yarn add @babel/preset-react -D
```
- To inject the traspiled file to html we'll use:
```
yarn add html-webpack-plugin -D
```

**News of React 17**
- You don't need more to import React from react dependency on all jsx files.
- Now it is possible make a setting to do it automatic. So on babel.config.js set the runtime attribute for @babel/preset-react
```
...
['@babel/preset-react', {
    runtime: 'automatic'
}]
...
```

## Webpack
- Allow us import several kind of files like css, hbs, sass and others, and transpile it for the browsers.

**Add dependencies**
```
yarn add webpack webpack-cli babel-loader -D
```

- Create the file webpack.config.js where will be all the settings to import modules.

**An important set up**
You can choose if the webpack run in a development or production environment.
For that you need to use the mode option and set it like development or production.

**webpack-dev-server**
We'll use this dependency to automate our webpack flux. This way it not more necessary compile everytime before run the application.
```
yarn add webpack-dev-server -D
```
Add a devServer option on webpack.config.js

**Running code with css**
For this we need to add two loaders:
```
yarn add style-loader css-loader -D

Add it on webpack rules:

{
    test: /\.css$/,
    exclude: /node_modules/,
    use: ['style-loader', 'css-loader'] 
}
```

## Source maps
Webpack's feature that allow us to see the original code at the moment of fix some error, for example, and not the transpiled file. That way we can find errors more quickly.
Add the follow option on webpack.config:
```
devtool: 'eval-source-map'
```