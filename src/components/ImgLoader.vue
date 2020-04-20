<template>
	<view>
		<image @click="handleClick" class="img" :src="src"></image>
	</view>
</template>

<script>
	export default {
		name: 'ImgLoader',
		props: {
			src: String
		},
		data() {
			return {
				msg: 'Hi Parent!'
			}
		},
		methods: {
			handleClick() {
				this.$emit('clickBy', this.src);
			}
		}
	}
</script>

<style>
  .img {
		width: 100px;
		height: 100px;
	}
</style>
