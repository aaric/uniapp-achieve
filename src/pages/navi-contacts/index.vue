<template>
	<view class="content">
		<view class="contacts-tab">
			<view class="contacts-tab-title">
				<view class="contacts-tab-title-list">
					<uni-segmented-control :current="current" :values="items.map(item=>item.title)"
						@clickItem="onClickItem"
						styleType="text"
						activeColor="#4ecf4c">
					</uni-segmented-control>
				</view>
				<view class="iconfont icon-search contacts-tab-title-search"></view>
			</view>
			<view class="contacts-tab-content">
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

<style lang="scss" scoped>
	.contacts-tab {
		.contacts-tab-title {
			position: relative;
			.contacts-tab-title-list {
				width: 60%;
				margin: 0 auto;
			}
			.contacts-tab-title-search {
				position: absolute;
				top: 50%;
				right: 5%;
				transform: translateY(-50%);
			}
		}
	}
</style>
