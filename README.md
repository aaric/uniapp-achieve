# uniapp-achieve

> [DCloud `uni-app` 微信小程序开发框架。](https://uniapp.dcloud.io/quickstart)

## 搭建项目框架

### 初始化项目

```node
vue create -p dcloudio/uni-preset-vue uniapp-achieve2
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
