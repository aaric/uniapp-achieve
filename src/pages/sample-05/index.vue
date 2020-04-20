<template>
	<view class="content">
		<img-loader @clickBy='handleChildClick' :src="src1"></img-loader>
		<img-loader @clickBy='handleChildClick' :src="src2"></img-loader>
	</view>
</template>

<script>
	import ImgLoader from '@/components/ImgLoader.vue'
	
	export default {
		components: {
			ImgLoader
		},
		data() {
			return {
					src1: 'http://www.easyicon.net/api/resizeApi.php?id=1174114&size=128',
					src2: 'http://www.easyicon.net/api/resizeApi.php?id=1173679&size=128'
			}
		},
		methods: {
			handleChildClick(msg) {
				console.log(msg)
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
