<template>
	<view class="content" catchtouchmove='true'>
		<image src="../../static/itemstwo.png" class="imgss"></image>
		<Mytabbar :selected="selected"></Mytabbar>
	</view>
</template>

<script>
	import Mytabbar from '../../custom-tab-bar/index.vue'
	export default {
		data() {
			return {
				selected:4
			};
		},
		components:{
			Mytabbar
		}
	}
</script>

<style lang="scss" scoped>
.imgss{
	width: 750rpx;
	height: 100vh;
}
</style>
