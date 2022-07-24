<template>
	<view>
		<image src="../../static/banner.png" class="img" @tap="showlist"></image>
		<form @submit="formSubmit" @reset="formReset" class="admissionform" :style="{height:formheight+'px'}">
			<view class="names">
				<view class="name">姓名:</view>
				<input class="uni-input" name="input" placeholder="请填写姓名" v-model="list.name" />
			</view>
			<checkbox-group name="checkbox">
				<label>
					<checkbox value="checkbox1" /><text>女士</text>
				</label>
				<label style="margin-left: 30rpx;">
					<checkbox value="checkbox2" /><text>先生</text>
				</label>
			</checkbox-group>
			<view class="names">
				<view class="name">身份证号码:</view>
				<input class="uni-input" name="input" placeholder="请填写身份证号码" />
			</view>
			<view class="names">
				<view class="name">手机号码:</view>
				<input class="uni-input" name="input" placeholder="请填写手机号码" v-model="list.tel" />
			</view>
			<view class="names">
				<view class="name">前端阶段:</view>
				<input class="uni-input" name="input" placeholder="请填写前端阶段" />
			</view>
			<view class="names">
				<view class="name">家庭地址:</view>
				<input class="uni-input" name="input" placeholder="请填写家庭地址" />
			</view>
			<view class="names">
				<view class="name">出生日期:</view>
				<input class="uni-input" name="input" placeholder="请填写出生日期" />
			</view>
			<view class="names">
				<view class="name">学历:</view>
				<input class="uni-input" name="input" placeholder="请填写学历" />
			</view>
			<view class="names">
				<view class="name">专业:</view>
				<input class="uni-input" name="input" placeholder="请填写专业" />
			</view>
			<view class="names">
				<view class="name">微信号:</view>
				<input class="uni-input" name="input" placeholder="请填写微信号" />
			</view>
			<view class="names">
				<view class="name">QQ号:</view>
				<input class="uni-input" name="input" placeholder="请填写QQ号" />
			</view>
			<view class="names">
				<view class="name">工作时间:</view>
				<input class="uni-input" name="input" placeholder="请填写工作时间" />
			</view>
			<view class="names">
				<view class="name">工作经历:</view>
				<input class="uni-input" name="input" placeholder="请填写工作经历" />
			</view>
			<view class="names">
				<view class="name">培训经历:</view>
				<input class="uni-input" name="input" placeholder="请填写培训经历" />
			</view>
			<view class="names">
				<view class="name">期望薪值:</view>
				<input class="uni-input" name="input" placeholder="请填写期望薪值" />
			</view>
		</form>
	
	</view>
</template>

<script>
	export default {
		data() {
			return {
				formheight:0,
				list:{name:'',tel:''}
			};
		},
		methods:{
			showlist(){
				console.log(this.list)
			}
		}
	}
</script>

<style lang="scss" scoped>
.img{
	width: 750rpx;
	height: 320rpx;
	border:none;
}
.admissionform{
	display: block;
	width: 750rpx;
	height: 100%;
	padding-left: 50rpx;
	padding-right: 50rpx;
	box-sizing: border-box;
	line-height: 100rpx;
	height: 100rpx;
	font-size: 32rpx;
	
}
.names{
	display: flex;
	flex-direction: row;
	align-items:center;
	border-bottom: 1px solid #f0f0f0;
	.name{
		width: 200rpx;
	}
	.uni-input{
		width:400rpx ;
		padding-left: 20rpx;
		color:#ccc;
		
	}
}

</style>
