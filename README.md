# uniapp-achieve

[![license](https://img.shields.io/badge/license-MIT-green.svg?style=flat&logo=github)](https://www.mit-license.org)
[![nodejs](https://img.shields.io/badge/node.js-13.12.0-brightgreen.svg?style=flat&logo=node.js)](https://nodejs.org)
[![release](https://img.shields.io/badge/release-0.6.0-blue.svg)](https://github.com/aaric/uniapp-achieve/releases)

> [DCloud `uni-app` 微信小程序开发框架。](https://uniapp.dcloud.io/quickstart)

## 搭建项目框架

### 初始化项目

```node
vue create -p dcloudio/uni-preset-vue uniapp-achieve
```

### 运行微信小程序项目

```node
npm run dev:mp-weixin
```

### 编译打包项目

```node
npm run build:mp-weixin
```

## 相关配置

### 支持sass语法

```node
npm i node-sass sass-loader -D
```

```html
<style lang="scss">
	.content {
		.sass {
			background-color: $uni-color-primary;
		}
	}
</style>
```

## 附录：用户自定义配置

参考[官方配置手册](https://cli.vuejs.org/config/)。

```bash
# create branch
git checkout -b dev-aaric

# commit code
git add .
git commit -m '0.6.0 components'
git push --set-upstream origin dev-aaric

# rein master
git checkout master
git fetch
git pull
git branch -d dev-aaric
```
