<script>
	export default {
		onLaunch: function() {
			console.log('App Launch')
		},
		onShow: function() {
			console.log('App Show')
		},
		onHide: function() {
			console.log('App Hide')
		},
		globalData: {
			customTilte: 'hello world'
		}
	}
</script>

<style>
	/*每个页面公共css */
	@import "./static/iconfont.wxss";
</style>
