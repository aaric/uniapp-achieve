<template>
	<view class="content">
		首页
	</view>
</template>

<script>
	export default {
		mounted() {
			this.request({
				url: 'http://jsonplaceholder.typicode.com/users'
			})
			.then(list=>{
				console.log(list)
			})
		}
	}
</script>

<style>
</style>
