<template>
	<view class="main">
		<image src="../../static/banner.png" class="header" @tap="goadmission"></image>
		<view class="itemsclass">
			<view class="itemclass" @tap="mengban">
				<image src="../../static/tiger.png" class="itemimg" ></image>
				<view class="text">教学管理</view>
			</view>
			<view class="itemclass" @tap="mengban">
				<image src="../../static/tiger.png" class="itemimg"></image>
				<view class="text">签署协议</view>
			</view>
			<view class="itemclass" @tap="mengban">
				<image src="../../static/tiger.png" class="itemimg"></image>
				<view class="text">咨询帮助</view>
			</view>
		</view>
		<view class="stars">
			<view class="title">名人堂</view>
			<scroll-view  scroll-y="true" class="scrolly" :style="{height:clientheights+'px'}">
				<view class="scrollitems">
					<image src="../../static/items.png" class="starimg" @tap="godatailtwo"></image>
					<image src="../../static/itemsfour.png" class="starimg" @tap="godatailtwo"></image>
					<image src="../../static/items.png" class="starimg" @tap="godatailtwo"></image>
					<image src="../../static/itemsfour.png" class="starimg" @tap="godatailtwo"></image>
					<image src="../../static/items.png" class="starimg" @tap="godatailtwo"></image>
					<image src="../../static/itemsfour.png" class="starimg" @tap="godatailtwo"></image>	
				</view>
			</scroll-view>
		</view>
		<view class="meng" v-show="mengshow"></view>
		<image src="../../static/itemsthree.png" class="mengimg" @tap="closemeng" v-show="mengshow"></image>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				clientheights:0,
				mengshow:false
			};
		},
		onReady() {
			uni.getSystemInfo({
				success:(res)=>{						
						this.clientheights = res.windowHeight - 430 ;
				}
			})
			
		},
		methods:{
			mengban(){
				this.mengshow = true;
			},
			closemeng(){
				this.mengshow = false;
			},
			goadmission(){
				uni.navigateTo({
					url:'../asmissionform/asmissionform'
				})
			},
			godatailtwo(){
				uni.navigateTo({
					url:'../detailtwo/detailtwo'
				})
			}
		}
	}
</script>

<style lang="scss" scoped>
.main{
	width: 750rpx;
	height: 100vh;
	box-sizing: border-box;
	background-color: #ececec;
	.header{
		background: url('../../static/banner.png') no-repeat;
		background-size: 100% 100%;
		width: 750rpx;
		height: 320rpx;
		box-sizing: border-box;
	}
	.itemsclass{
		width: 750rpx;
		display: flex;
		flex-direction: row;
		justify-content: space-between;
		box-sizing: border-box;
		margin-top: 50rpx;
		.itemclass{
			width: 100%;
			height: 100%;
			box-sizing: border-box;
			display: flex;
			flex-direction: column;
			justify-content:space-between;
			align-items:center ;
			.itemimg{
				width: 200rpx;
				height: 200rpx;
			}
			.text{
				width: 200rpx;
				height: 80rpx;
				line-height: 80rpx;
				text-align: center;
			}
		}
	}
}
.title{
	width: 100%;
	height: 80rpx;
	line-height: 80rpx;
	margin-bottom: 20rpx;
	font-size: 40rpx;
	font-weight: 600;
	padding-left: 56rpx;
	box-sizing: border-box;
	
}
.scrolly{
		
		width: 750rpx;
		height: 200rpx;
	}
	.scrollitems{
		display: flex;
		flex-direction: row;
		justify-content:space-evenly;
		align-content :center;
		flex-wrap:wrap;
		width: 750rpx;
	
	}
.starimg{
	width: 300rpx;
	height: 400rpx;
	margin-bottom: 20rpx;
}
.meng{
	position: fixed;
	top: 0;
	left:0;
	width: 750rpx;
	height: 100vh;
	background-color: black;
	opacity: 0.5;
	z-index: 99999;
}
.mengimg{
	position: fixed;
	top: 15vh;
	left:100rpx;
	width: 550rpx;
	height: 50vh;
	z-index: 9999999;
	
}
</style>
