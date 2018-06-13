# a-react-story
Quick presentation on storybook and React.

## Add Yarn

```bash
yarn init
```

## [Add React](https://reactjs.org/docs/add-react-to-an-existing-app.html)

```bash
yarn add react react-dom
```

## Enabling ES6 and JSX

### Reactjs.org recommends using React with Babel to let you use ES6 and JSX in your JavaScript code. 
- ES6 is a set of modern JavaScript features that make development easier.
- JSX is an extension to the JavaScript language that works nicely with React.

### The Babel setup instructions explain how to configure Babel in many different build environments. 
```bash
yarn add -D babel-core
```

###Make sure you install and enable in your .babelrc:
 - babel-preset-react 
```bash
yarn add -D babel-preset-react
```
 - babel-preset-env 
```bash
yarn add -D babel-preset-env
```

## Add webpack
```bash
yarn add -D webpack 
```
```bash
yarn add -D webpack-cli
```
```bash
yarn add -D webpack-dev-server
```
```bash
yarn add -D style-loader
```
```bash
yarn add -D css-loader 
```
```bash
yarn add -D babel-loader 
```

## [Development Build](https://webpack.js.org/guides/development/)

### cleanup before each build
```bash
yarn add -D html-webpack-plugin clean-webpack-plugin
```
Add 
```js
  plugins: [
    new CleanWebpackPlugin(['dist']),
    new HtmlWebpackPlugin({
      title: 'Development'
    }),
  ],
```
to webpack.config.js obj.

### get sourcemaps for better error messages

Add
```js
 devtool: 'inline-source-map',
```
to webpack.config.js obj.

### have dev server open new browser tab on start
Update start:dev script in package.json.
```json
  "scripts": {
    "start:dev": "webpack-dev-server --mode development --open"
  },
```

## Production Build
```bash
yarn add -D webpack-merge
```