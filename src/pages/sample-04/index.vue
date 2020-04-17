<template>
	<view class="content">
		<view @click="printSalary(chinaSalary)">{{name}} - {{chinaSalary}}</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				name: 'Nick',
				salary: 5000
			}
		},
		onLoad() {

		},
		methods: {
			printSalary(salary) {
				console.log('salary: ' + salary);
			}
		},
		computed: {
		  chinaSalary() {
				return '￥' + this.salary;
			}
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
