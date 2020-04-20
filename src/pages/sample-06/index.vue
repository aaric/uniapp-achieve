<template>
	<view class="content">
		<view>{{msg}}</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				msg: this.baseUrl
			}
		},
		onLoad() {
			console.log(this.baseUrl)
			console.log(getApp().globalData.customTilte)
		}
	}
</script>

<style>
	.content {
		text-align: center;
		height: 400upx;
	}
</style>
