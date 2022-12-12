# docsify

## docsify 安装
```yml
npm i docsify-cli -g
```
## 初始化本地项目
```yml
docsify init ./docs
```
- 初始化之后会出现 docs 文件夹
- 主要用到 index.html,相当于配置项，定义功能配置、插件的使用
- README.md 是首页的内容

##  本地预览 
```yml
 docsify serve docs
```

## 浏览器访问
http://localhost:3000


## Github 部署
- push 文件夹到 github远端
- settings - pages -save
- 生成专属链接
- 访问 https://doushuo.github.io/md-note/