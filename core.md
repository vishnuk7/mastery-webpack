#### Webpack Core

###### Entry
The first javascript file to load to "kick-off" your app

webpack uses this as the starting

```js
module.export = {
  entry: "./index.js"
}
```
Tells webpack **what**(files) to load for the browser Compliments the **Output** property 

###### Output
```js
module.export = {
  entry: "./index.js",
  output: { 
    path:"./dist",
    filename: "bundle.js"
  }
}
```

Tells webpack **where** and **how** to distribute bundles (compilations). Works with Entry

###### Loaders and rules
Tells webpack how to modify file before its added to dependency graph

Loaders are also javascript modules(function) that takes the source file, and returns it in a [modified] state.

```js
module:{
  rules:[
    {test:/\.ts$/, use: `ts-loader`},
    {test:/\.js$/,use: `babel-loader`}
    {test:/\.css$/,use:`css-loader`}
  ]
}
```

if webpack find some pattern `test:/\.ts$/` then apply this `use:"ts-loader"`

**loaders**
```js
module:{
  rules:[
    {
      test:regex,
      use:(Array|String|Function),
      include:RegExp[],
      exclude:RegExp[],
      issuer:(RegExp,String)[],
      enforece:"pre"|"post"
    }
  ]
}
```

* test
A *regular expression* that instructs the compiler which file to rub the loader against

* use
An array/string/function that return loaders objects.

* enforce
Can be "pre" or "post", tells webpack to run this rule before or after all  other rule

* include
An *array of regular expression* that instrcut the compiler which folders/files to include.
Will only search paths provider with the include

* exclude 
An *array of regular expression* that instructs the compiler which folders/files to ignore