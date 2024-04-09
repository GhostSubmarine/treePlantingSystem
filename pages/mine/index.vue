<template>
	<view class="page">
		<image class="avator-img" src="../../static/mine/wImage@1x.png" alt="" :draggable="false" />
		<text class="avator-name">{{avatorName}}</text>
		<view class="row">
			<image class="row-img" 
				src="../../static/mine/fas fa-align-left@1x.png" 
				draggable="false" />
			<text>订单管理</text>
		</view>
		<view class="row">
			<image class="row-img" 
				src="../../static/mine/fas fa-address-card Jut3Y4v@1x.png" 
				draggable="false" />
			<text>我的证书/树木照片</text>
		</view>
		<view class="row">
			<image class="row-img" 
				src="../../static/mine/md-help 4SG89L2@1x.png" 
				draggable="false" />
			<text>联系客服</text>
		</view>
		<view class="row">
			<image class="row-img" 
				src="../../static/mine/md-assignment_late@1x.png" 
				draggable="false" />
			<text>用户指南</text>
		</view>
		<view class="row">
			<image class="row-img" 
				src="../../static/mine/md-assignment_returned@1x.png" 
				draggable="false" />
			<text>碳减排</text>
		</view>
		<view class="row">
			<image class="row-img" 
				src="../../static/mine/md-settings A0zvrXV Copy 2@1x.png" 
				draggable="false" />
			<text>绑定/修改手机号</text>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				avatorName: '昵称'
			}
		},
		methods: {
			
		}
	}
</script>

<style lang="less">
@font16: 31rpx;
@font14: 27rpx;
@font18: 35rpx;
@font12: 23rpx;
.page {
	display: flex;
	flex-direction: column;
	background-color: rgba(255, 255, 255, 1);
	color: rgba(0, 0, 0, 1);
	.avator-img {
		width: 192.3rpx;
		height: 192.3rpx;
		margin: 10rpx auto 0 auto;
		border-radius: 50%;
	}
	.avator-name {
		margin: 25rpx auto 28.85rpx auto;
		font-size: @font16;
	}
	.row {
		height: 103.85rpx;
		font-size: @font14;
		margin-left: @font14;
		display: flex;
		align-items: center;
		gap: @font12;
		.row-img {
			height: 46.154rpx;
			width: 46.154rpx;
		}
	}
}
</style>
