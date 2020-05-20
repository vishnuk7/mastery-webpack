#### Scratch

```json
"script":{
  "webpack":"webpack"
}
```

how this script code are running there is a folder in node_modules which is `.bin` which contains exetuable or binary file rest you can understand it.

It start with looking for entry point
by default it look inside the `./src` folder for entry point

```json
"script":{
  "webpack-start":"webpack",
  "dev":"npm run webpack-start -- --mode development",//compose
}
```

```json
"script":{
  "webpack-start":"webpack",
  "dev":"npm run webpack-start -- --mode development",//compose
  "prod":"npm run webpack-start -- --mode production"
}
```

#### Debug Webpack
```json
"script":{
  "webpack-start":"webpack",
  "dev":"npm run webpack-start -- --mode development",//compose
  "prod":"npm run webpack-start -- --mode production",
  "dev:debug":"npm run debug -- --mode production",
  "prod:debug":"npm run debug -- --mode development"
}
```

```json
"script":{
  "debugthis":"node --inspect --inspect-brk ./src/index.js",
}
```
above command help you inspect your code which give you url with the help that of url you can use chrome debug it

>by default build asset go into `dist` folder

#### Adding watch mode
```json
"script" => {
  "dev":"npm run webpack-start -- --mode development --watch",
}
```
Webpack bundle only which those element which are using other are going to elminate

`webpack.config.js`

```js
module.export = {
    
}
```