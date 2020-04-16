<template>
	<view class="content">
		<view class="rpx">rpx</view>
		<view class="vw">vw</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello xx!'
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style>
	.rpx {
		/* 小程序单位 -> screen width = 750rpx */
		width: 750rpx;
		height: 100px;
		background-color: red;
	}
	.vw {
		/* h5单位 -> screen width = 100vw, screen height = 100vw */
		width: 50vw;
		height: 25vw;
		background-color: orange;
	}
</style>
