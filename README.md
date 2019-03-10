# create_react_app

npm init

git init

npm install -g webpack webpack-cli


npm install --save-dev babel-core babel-loader babel-polyfill babel-preset-es2015 babel-preset-react babel-plugin-transform-decorators-legacy babel-plugin-transform-class-properties @babel/core

npm install @babel/core babel-loader @babel/preset-env @babel/preset-react --save-dev

npm install --save react react-dom prop-types redux react-redux

create webpack.config.js :
const path = require("path");
module.exports = {
  entry: "./src/index.js",
  output: {
    path: path.join(__dirname, "/dist"),
    filename: "index_bundle.js"
  },
  module: {
    rules: [
      {
        test: /\.js$/,
        exclude: /node_modules/,
        use: {
          loader: "babel-loader"
        },
      },
      {
        test: /\.css$/,
        use: ["style-loader", "css-loader"]
      }
    ]
  }
};

create .babelrc
{
  "presets": ["react", "es2015"],
  "plugins": [
    "transform-decorators-legacy",
    "transform-class-properties"
  ]
}

