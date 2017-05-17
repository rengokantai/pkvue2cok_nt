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
