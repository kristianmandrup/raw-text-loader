# raw-text-loader
Webpack loader to load pure raw text.

## Install & Usage

`npm i raw-text-loader --save-dev`

Add loader config to your webpack config file, f.ex `webpack.base.conf.js`

```js
module: {
    loaders: [
      {
        test: /\.txt$/,
        loader: 'raw-text'
      },
      // ...
}
```

## Use case

In a recent Web app, I wanted to load text blocks from files instead of inlining or making a server request. The text will thus be inlined at compile time by Webpack :)

```js
  code: {
    vm: require('raw!../examples/breadcrumb/vm.js.txt'),
    view: require('raw!../examples/breadcrumb/view.html.txt')
  }
```

In this case, I used these files to display highlighted code examples.

## Similar projects

[text-loader](https://www.npmjs.com/package/text-loader)
[raw-loader](https://github.com/webpack/raw-loader)

These loaders both return the file content wrapped with: `module.exports = JSON.stringify(content);`.

## License

MIT