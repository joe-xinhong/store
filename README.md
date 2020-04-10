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

###### VUE CLI 3 默认端口修改
*所在目录：node_modules\@vue\cli-service\lib\commands*<br>
*需要修改的文件：serve.js*<br>
const defaults = {<br>
  host: '0.0.0.0',<br>
  port: 8080,<br>
  https: false<br>
}
