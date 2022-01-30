# Markdown Loader 
A markdown loader for webpack using markdown-it.

## Installation
```
npm install --save-dev do-markdown-loader
```

## Usage

```
const path = require('path')
const HtmlWebpackPlugin = require('html-webpack-plugin')

module.exports = {
    entry: {
        index: './src/js/index.js'
    },

    module: {
        rules: [
            {
                test: /\.md$/,
                use: [
                {
                    loader: 'html-loader'
                },
                {
                    loader: 'do-markdown-loader',
                    options: {
                        html: true
                    }
                }],
            }
        ]
    },

    plugins: [
      new HtmlWebpackPlugin({
        filename: 'index.html',
        template: './src/views/index.html',
      })
    ]
}
```
