Source : [Generator authoring](https://yeoman.io/authoring/index.html)  

```cmd
npm install -g yo
```

Create a directory generator-[generator name]  

Create a package.json file :
```cmd
Execute npm init
```

Ensure last version of yeoman generator
```cmd
npm install --save yeoman-generator
```

Link local module to global npm :  
```cmd
npm link
```


##Install Dependencies
```cmd
npm install yosay
npm install mkdirp
```

##Install Development Dependencies
```cmd
npm install --save-dev yeoman-assert
npm install --save-dev yeoman-test
npm install --save-dev mocha
npm install --save-dev nyc
npm install --save-dev vsts-coverage-styles
```
