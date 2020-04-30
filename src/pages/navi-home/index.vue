<template>
	<view class="content">
		<text class="iconfont icon-chat"></text>
		<view class="sass">
			首页
		</view>
		<view>
			<uni-badge text="1"></uni-badge>
			<uni-badge text="2" type="success"></uni-badge>
			<uni-badge text="3" type="primary" :inverted="true"></uni-badge>
		</view>
	</view>
</template>

<script>
	import {uniBadge} from '@dcloudio/uni-ui'
	
	export default {
		components: {
			uniBadge
		},
		onLoad() {
			// 1.weixin
			wx.request({
				url: 'http://jsonplaceholder.typicode.com/users',
				success(res) {
					console.log(res)
				}
			})
			
			// 2.uni-api
			uni.request({
				url: 'http://jsonplaceholder.typicode.com/users'
			})
			.then(data=>{
				var [error, res] = data
				console.log(res)
			})
		}
	}
</script>

<style lang="scss">
	.content {
		.sass {
			background-color: $uni-color-primary;
		}
	}
</style>
