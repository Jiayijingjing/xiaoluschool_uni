<template>
	<view class="tabbar">
		<view class="tabbar_list">
			<view class="tabbar_list_ul">
				<view class="tabbar_list_ul_li" v-for="(item,index) in tabBar.list" :key="index" @tap="changetabbar(index)" v-if="tabBar.list.length>0">
					<view class="tabbar_list_li_icon">
						<image  :src="selected == index? item.selectedIconPath : item.iconPath"  class="tabbarimg" ></image>
						
					</view>
					<view class="tabbar_list_li_name" :class="selected == index?'blue':'black'">{{item.text}}</view>
				</view>
				
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		props:{
			selected:Number
		},
		data() {
			return {
				tabBar:{
					list:[{
						pagePath:'/pages/index/index',
						iconPath:'../static/main.png',
						selectedIconPath:'../static/mainb.png',
						text:'首页'
					},{
						pagePath:'/pages/qustions/qustions',
						iconPath:'../static/fenlei.png',
						selectedIconPath:'../static/fenleidark.png',
						text:'刷题'
					},{
						pagePath:'/pages/process/process',
						iconPath:'../static/text.png',
						selectedIconPath:'../static/textdark.png',
						text:'流程'
					},{
						pagePath:'/pages/contact/contact',
						iconPath:'../static/contact.png',
						selectedIconPath:'../static/contactdark.png',
						text:'协议'
					},{
						pagePath:'/pages/my/my',
						iconPath:'../static/wo.png',
						selectedIconPath:'../static/wob.png',
						text:'我的名片'
					}]
				},
				
				
			}
			
		},
		
		methods:{
			changetabbar(index){
				
				uni.switchTab({
					url: this.tabBar.list[index].pagePath
				})
				
			}
		},
		
		
	}
</script>

<style lang="scss" scoped>
.tabbar{
	width: 100%;
	position:fixed;
	box-sizing: border-box;
	z-index: 999999;
	
}
.tabbar_list{
	width: 100%;
	position: fixed;
	left: 0;
	bottom: 0;
	box-shadow: 0px -12px 37px 0px rgba(230, 235, 243, 0.9);
	border-top-left-radius: 30rpx;
	border-top-right-radius: 30rpx;
	box-sizing: border-box;
}
.tabbar_list_ul{
	width: 100%;
	height: 100%;
	display: flex;
	justify-content:space-between;
	box-sizing: border-box;
	background: white;
}
.tabbar_list_ul_li{
	padding-top: 8rpx;
	display: flex;
	flex-direction: column;
	justify-content:space-between;
	align-items:center;
	width: 150rpx;
	height:100rpx;
}
.tabbar_list_li_icon{
	width: 56rpx;
	height: 56rpx;
}

.tabbarimg{
	width: 56rpx;
	height: 56rpx;
}
.tabbar_list_li_name{
	width: 100%;
	height: 40rpx;
	line-height: 40rpx;
	text-align: center;
	font-size: 28rpx;
	font-family: Microsoft YaHei;
}
.blue{
	color: #8ab2e3;
}
.black{
	color: #2f2f2f;
}
</style>

