<template>
	<view class="content">
		<form-content>
			<input placeholder="Where are you from?" /><br/>
			<checkbox /><br/>
			<radio /><br/>
		</form-content>
	</view>
</template>

<script>
	import FormContent from '@/components/FormContent.vue'
	
	export default {
		components: {
			FormContent
		}
	}
</script>

<style>
	.content {
		text-align: center;
		height: 400upx;
	}
</style>
