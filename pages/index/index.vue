<template>
		<view class="container">
			<image class="image-bg" src="../../static/bg.png" />
			<view class="header">
				<view class="home_title">小鹿前端学院</view>
				<view class="home_school">入学信息入口</view>
				<view class="home_class">
					<view class="texts">查看班级权益</view>
					<image class="home_img" src="../../static/fangda.png"></image>
				</view>
			</view>
			<view class="items">
				<view class="item">
					<image src="../../static/itemsthree.jpeg"></image>
				</view>
				<view class="item">
					<image src="../../static/itemone.png"></image>
				</view>
				<view class="item">
					<image src="../../static/itemsfour.png"></image>
				</view>
				<view class="item">
					<image src="../../static/items.png"></image>
				</view>
				<view class="item">
					<image src="../../static/itemone.png"></image>
				</view>
				<view class="item">
					<image src="../../static/itemsthree.jpeg" ></image>
				</view>
			</view>
			<Mytabbar :selected="selected" ></Mytabbar>
		</view>
		
	
</template>

<script>
	import Mytabbar from '../../custom-tab-bar/index.vue'
	export default {
		data() {
			return {
				selected:0 
			}
		},
		onLoad() {
			
		},
		components:{
			Mytabbar
		},
		methods: {

		}
	}
</script>

<style lang="scss" scoped>
	
.container{
	width: 750rpx;
}
.header{
	padding-left: 30rpx;
	padding-right: 30rpx;
}
.home_title{
	height: 80rpx;
	line-height: 80rpx;
	color: #536aff;
	font-size: 50rpx;
	font-weight: 500;
}
.home_school{
	height: 80rpx;
	line-height: 80rpx;
	color: #707070;
	font-size: 40rpx;
}
.home_class{
	width: 350rpx;
	height: 50rpx;
	line-height: 50rpx;
	background-color:#536aff;
	color:white;
	display: flex;
	flex-direction: row;
	align-items:center;
	border-radius: 12rpx;
}
.texts{
	width: 220rpx;
	box-sizing: border-box;
	font-size: 24rpx;
	height: 34rpx;
	line-height: 34rpx;
	
	border-right: 2px solid white;
	text-align: center;
}
.home_img{
	width: 40rpx;
	height: 40rpx;
	margin-left: 48rpx;
}
.items{
	width: 750rpx;
	display: flex;
	flex-direction: row;
	flex-wrap:wrap;
	justify-content:space-evenly;
	margin-top: 20rpx;
	padding-bottom: 130rpx;
}

.item {
	width: 330rpx;
	height: 450rpx;
	margin-top: 20rpx;
	border-radius: 12px;
	image{
		width: 330rpx;
		height: 450rpx;
		border-radius: 12rpx;
	}
}
</style>
