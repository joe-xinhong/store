# store

## Project setup
```
yarn install
```

### Compiles and hot-reloads for development
```
yarn serve
```

### Compiles and minifies for production
```
yarn build
```

### Lints and fixes files
```
yarn lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).


#### 打包发布
1.修改 router/index.js文件<br>
mode: 'history', ---> mode:'hash',

2.yarn build
