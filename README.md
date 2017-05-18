# pkvue2cok_nt

```
vue init webpack foldername
```

or simple,
```
gurghet/webpack
```

change webpack.prod.conf.js
```
webpack.DefinePlugin
webpack.optimize.UglifyJsPlugin
webpack.optimize.OccurrenceOrderPlugin
```

then change output
```
output{
  path: config.build.assetRoot,
  filename: utils.assetsPath('shaker.js')
}
```
Our component will normally contain the Vue library inside; if you want to use the component in a Vue project, you don't need this, as it would be duplicated code. You can tell Webpack to just search for dependencies externally and not include them. Add the following property in the webpack.prod.js file you just modified before plugins:
```
externals: {
  'vue': 'Vue'
}
```
As the last change, I would suggest modifying the folder in which the minified file gets saved. In the config/index.js file, edit the following line:
```
assetsSubDirectory: 'static'
```
Swap the preceding line with the following code:
```
assetsSubDirectory: '.',
```
