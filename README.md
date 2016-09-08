# angular-core-export-overwrite

Reproduction for [webpack/webpack#2970](https://github.com/webpack/webpack/issues/2970)

Steps to reproduce:

```
$ webpack
$ node dist/main.js
```

Expected: A console output
Actual: 
```
C:\Users\kairu\Source\Repos\angular-core-webpack-export-overwrite\dist\main.js:41
/******/                Object.defineProperty(exports, name, {
                               ^

TypeError: Cannot redefine property: a
    at Function.defineProperty (native)
    at Function.__webpack_require__.d (C:\Users\kairu\Source\Repos\angular-core-webpack-export-overwrite\dist\main.js:41:19)
    at Object.<anonymous> (C:\Users\kairu\Source\Repos\angular-core-webpack-export-overwrite\dist\main.js:12855:54)
    at __webpack_require__ (C:\Users\kairu\Source\Repos\angular-core-webpack-export-overwrite\dist\main.js:20:30)
    at Object.AnimationKeyframe.AnimationKeyframe.styles.offset (C:\Users\kairu\Source\Repos\angular-core-webpack-export-overwrite\dist\main.js:12351:68)
    at __webpack_require__ (C:\Users\kairu\Source\Repos\angular-core-webpack-export-overwrite\dist\main.js:20:30)
    at Object.<anonymous> (C:\Users\kairu\Source\Repos\angular-core-webpack-export-overwrite\dist\main.js:15334:72)
    at __webpack_require__ (C:\Users\kairu\Source\Repos\angular-core-webpack-export-overwrite\dist\main.js:20:30)
    at exports.s (C:\Users\kairu\Source\Repos\angular-core-webpack-export-overwrite\dist\main.js:64:18)
    at Object.<anonymous> (C:\Users\kairu\Source\Repos\angular-core-webpack-export-overwrite\dist\main.js:67:10)
```
