<template>
		<view class="container">
			<view class="header">
				<view class="home_title">小鹿前端学院</view>
				<view class="home_school">入学信息入口</view>
				<view class="home_class">
					<view class="texts">查看班级权益</view>
					<image class="home_img" src="../../static/fangda.png"></image>
				</view>
			</view>
			<scroll-view  scroll-y="true" class="scroll-Y" :style="{height:clientheight+'px'}">
				<classitems></classitems>
			</scroll-view>
			<Mytabbar :selected="selected" ></Mytabbar>
		</view>
</template>

<script>
	import Mytabbar from '../../custom-tab-bar/index.vue'
	import classitems from '../items/items.vue'
	export default {
		data() {
			return {
				selected:0 ,
				clientheight:0
			}
		},
		onLoad() {
			
		},
		components:{
			Mytabbar,
			classitems
		},
		methods: {

		},
		onReady() {
			uni.getSystemInfo({
				success:(res)=>{
					let info = uni.createSelectorQuery().in(this).select('.header');
					info.boundingClientRect((data)=>{
						
						this.clientheight = res.windowHeight - data.height -150 ;
					}).exec(function(res){});
				}
			})
			
		}
	}
</script>

<style lang="scss" scoped>
	
.container{
	width: 750rpx;
	height: 100%;
	background: url('https://fawn.xuexiluxian.cn/api/profile/wechat/bgimg/bg.png') no-repeat;
	background-size: cover;
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
.scroll-Y {
		height: 870rpx;
		width: 750rpx;
		margin-top: 26rpx;
	}



</style>
