### Why Webpack?
When you create a web apps which have 1000+ modules to 
when some one access to the your web app then client 
request all the modules if that page is using to cause a web performance issue.

IIFE :- Immediately Invoked Function Expression

Treat Each file as IIFE (REVEALING MODULE)

When you treat you each file as IIFE then we can **safely** combine file without concern of scope collision!

*lots of IIFE's are slow*

ESM For Browser is very very very slow don't use it!

Webpack is a module bundler 
Lets you write any module format `commonJS, AMD, ESM` (mixed!), compiles them for the browser

Supports static async bundling

Rich, Vast, Ecosystem the most performant way to ship javascript today

###### Webpack - How to use it?
```javascript
module.exports = {
  entry:{
    vendor:"./src/vendors.ts",
    main:"./src/main.browser.ts"
  },
  output:{
    path: "dist",
    filename:"[name].bundel.js"
  }
}
```

Config
`(webpack.config.js) Yes, it's a module too!`

You can use with the help of webpack cli
`webpack <entru.js> <result.js> --colors --progress`
`webpack-dev-server --port=9000`

Node API
```javascript
let webpack = require("webpack");
//returns a compiler instance
webpack({
  //configuration object here! 
},functon(err,stats){
  //compilerCallback
  console.err(err);
})
```