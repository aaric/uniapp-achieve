<template>
	<view class="content">
		<view>{{ msg }}</view>
		<view>{{ salary }}</view>
		<view>{{ alone }}</view>
		<view>{{ person.name }}</view>
		<view>{{ person.skill }}</view>
		<view :data-color="color">color</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				msg: 'Hello uni-app!',
				salary: 5000,
				alone: true,
				person: {
					name: 'Nick',
					skill: 'java' 
				},
				color: 'red'
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style>
	.content {
		text-align: center;
		height: 400upx;
	}

	.logo {
		height: 200upx;
		width: 200upx;
		margin-top: 200upx;
	}

	.title {
		font-size: 36upx;
		color: #8f8f94;
	}
</style>
