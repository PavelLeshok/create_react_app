# create_react_app

npm init

git init

npm install -g webpack webpack-cli


npm install --save-dev babel-core babel-loader babel-polyfill babel-preset-es2015 babel-preset-react babel-plugin-transform-decorators-legacy babel-plugin-transform-class-properties @babel/core

npm install --save react react-dom prop-types redux react-redux

create webpack.config.js :
'use strict';
var path = require("path");
module.exports = {
    mode: 'development',
    entry: {
        "index": "./index.js"
    },
    output: {
        path: path.join(__dirname, "build"),
        filename: "[name].bundle.js"
    },
    module: {
        rules: [
            {
                test: /\.js$/,
                use: "babel-loader"
            }
        ]
    },
    devtool: "source-map",
    watch: true,
    watchOptions: {
        aggregateTimeout: 300
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

