# uniapp-achieve

[![license](https://img.shields.io/badge/license-MIT-green.svg?style=flat&logo=github)](https://www.mit-license.org)
[![nodejs](https://img.shields.io/badge/node.js-13.12.0-brightgreen.svg?style=flat&logo=node.js)](https://nodejs.org)
[![release](https://img.shields.io/badge/release-1.0.0-blue.svg)](https://github.com/aaric/uniapp-achieve/releases)

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
npm install sass-loader node-sass
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

## uni-ui 使用说明

> [参考`uni-ui`官方使用文档。](https://www.npmjs.com/package/@dcloudio/uni-ui)

### 安装

```node
npm install @dcloudio/uni-ui
```

### 使用示例

```javascript
import {uniBadge} from '@dcloudio/uni-ui'
//import uniBadge from '@dcloudio/uni-ui/lib/uni-badge/uni-badge.vue' //也可使用此方式引入组件
export default {
    components: {uniBadge}
}
```

```html
<uni-badge text="1"></uni-badge>
<uni-badge text="2" type="success" @click="bindClick"></uni-badge>
<uni-badge text="3" type="primary" :inverted="true"></uni-badge>
```

## 附录一：用户自定义配置

参考[官方配置手册](https://cli.vuejs.org/config/)。

## 附录二：GIT命令参考

```bash
# create branch
git checkout -b dev-aaric

# commit code
git add .
git commit -m '1.4.0 uni-segmented-control'
git push --set-upstream origin dev-aaric

# rein master
git checkout master
git fetch
git pull
git branch -D dev-aaric
```
