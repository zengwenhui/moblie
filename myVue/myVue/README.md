# self

> first Vue Project

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

For detailed explanation on how things work, checkout the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).

# 目录说明：
>  babelrc   //对babel的一些具备配置和依赖项说明
  {
  "presets": [
    ["env", { "modules": false }], //将一些ES6的语法经行编译的依赖
    "stage-2"
  ],
  "plugins": ["transform-runtime"],  //将一些ES6的方法经行转化的插件
  "comments": false,               //false转换后的代码不生成注释
  "env": {
    "test": {
      "presets": ["env", "stage-2"],
      "plugins": [ "istanbul" ]
    }
  }
}
> editorconfig  //对编辑器的一些具备设置
root = true
                    
[*]
charset = utf-8   //代码编码格式
indent_style = space   //缩进方式
indent_size = 2   //缩进大小
end_of_line = lf   
insert_final_newline = true
trim_trailing_whitespace = true


> eslintignore   //不对文件经行eslint规范检查的配置文件
build/*.js
config/*.js

> eslintrc.js   // eslint的一个配置文件

// http://eslint.org/docs/user-guide/configuring

module.exports = {
  root: true,
  parser: 'babel-eslint',
  parserOptions: {
    sourceType: 'module'
  },
  env: {
    browser: true,
  },
  // https://github.com/feross/standard/blob/master/RULES.md#javascript-standard-style
  extends: 'standard',    //继承规则   规则在上面的github可以查阅
  // required to lint *.vue files
  plugins: [
    'html'
  ],
  // add your custom rules here
  'rules': {            //对具体的规则经行修改
    // allow paren-less arrow functions
    'arrow-parens': 0,
    // allow async-await
    'generator-star-spacing': 0,
    // allow debugger during development
    'no-debugger': process.env.NODE_ENV === 'production' ? 2 : 0
  }
}

>gitgnore  //对git的配置  配置哪些文件不会提到git仓库中去
.DS_Store
node_modules/
dist/
npm-debug.log*
yarn-debug.log*
yarn-error.log*
>index.html  //打包后的文件会被插到index.html文件中来。

>package.json  //项目的配置文件
script  //执行的新命令
dependencies   //项目运行的依赖
devDependencies  //项目编译中的依赖