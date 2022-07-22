<script>
	export default {
		onLaunch: function() {
			console.log('App Launch')
			uni.hideTabBar();
		},
		onShow: function() {
			console.log('App Show')
			uni.hideTabBar();
		},
		onHide: function() {
			console.log('App Hide')
		}
	}
</script>

<style>
	/*每个页面公共css */
	.container{
		margin-top: 70px;
		
	}
	.image-bg {
	    position: absolute;
	    z-index: -1;
	    left: 0;
	    right: 0;
	    bottom: 0;
	    right: 0;
	    width: 100%;
	    height: 100%;
	}
</style>
