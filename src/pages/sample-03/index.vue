<template>
	<view class="content">
		<view v-for="(item, index) in fruits" :key="item.id" v-if="3 >= item.id">
			<view>{{item.id}} - {{item.name}}</view>
		</view>
		<view>
			<view>---------------</view>
			<view v-if="true">if</view>
			<view v-show="true">show</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				fruits: [
					{
						id: 1,
						name: '苹果'
					},
					{
						id: 2,
						name: '梨子'
					},
					{
						id: 3,
						name: '香蕉'
					},
					{
						id: 4,
						name: '芒果'
					},
					{
						id: 5,
						name: '菠萝'
					}
				]
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
</style>
