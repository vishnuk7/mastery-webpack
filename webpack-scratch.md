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

 