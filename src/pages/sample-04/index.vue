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
</style>
