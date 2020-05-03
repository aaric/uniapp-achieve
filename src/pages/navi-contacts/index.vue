<template>
	<view class="content">
		<uni-segmented-control :current="current" :values="items.map(item=>item.title)"
			@clickItem="onClickItem"
			styleType="text"
			activeColor="#4ecf4c">
		</uni-segmented-control>
		<view class="tab-content">
			<view v-show="0 == current">
				<contacts-friend></contacts-friend>
			</view>
			<view v-show="1 == current">
				<contacts-group></contacts-group>
			</view>
			<view v-show="2 == current">
				<contacts-device></contacts-device>
			</view>
		</view>
	</view>
</template>

<script>
	import {uniSegmentedControl} from '@dcloudio/uni-ui'
	
	import ContactsFriend from './contacts-friend/index.vue'
	import ContactsGroup from './contacts-group/index.vue'
	import ContactsDevice from './contacts-device/index.vue'
	
	export default {
		components: {
			uniSegmentedControl,
			ContactsFriend,
			ContactsGroup,
			ContactsDevice
		},
		data() {
			return {
				items: [
					{
						title: '好友'
					},
					{
						title: '群聊'
					},
					{
						title: '设备'
					}
				],
				current: 0
			}
		},
		methods: {
			onClickItem(e) {
				if (this.current != e.currentIndex) {
					console.log(e)
					this.current = e.currentIndex
				}
			}
		}		
	}
</script>

<style>
</style>
