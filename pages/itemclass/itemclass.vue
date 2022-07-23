<template>
	<view class="item">
		<image :src="urls"></image>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		props:['urls']
	}
</script>

<style lang="scss" scoped>
.item {
	width: 330rpx;
	height: 450rpx;
	margin-bottom: 20rpx;
	border-radius: 12px;
	image{
		width: 330rpx;
		height: 450rpx;
		border-radius: 12rpx;
	}
}
</style>

