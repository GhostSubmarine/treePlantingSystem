<template>
	<view class="page">
		<h6>
			个人信息
		</h6>
		<u--text :text="`姓名:${info.userName}`" style="margin: 10rpx 50rpx;"></u--text>
		<u--text :text="`姓名:${info.userName}`" style="margin: 10rpx 50rpx;"></u--text>
		<h6>
			树木信息
		</h6>
		<u--text :text="`树木编号:${info.no}`" style="margin: 10rpx 50rpx;"></u--text>
		<u--text :text="`树种:${info.type}`" style="margin: 10rpx 50rpx;"></u--text>
		<u--text :text="`所属:${info.onwer}`" style="margin: 10rpx 50rpx;"></u--text>
		<h6>
			账单信息
		</h6>
		<u--text :text="`认捐:${info.money}`" style="margin: 10rpx 50rpx;"></u--text>
		<u-button @click="goHome" type="primary" style="width: 50%; margin: 20rpx auto;" shape="circle" text="确认订单"></u-button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				info: {
					userName: 'xxx',
					phone: 'xxxx',
					no: 'xxxx',
					type: 'xxx',
					onwer: 'xxxx',
					money: 'xxx'
				}
			};
		},
		methods: {
			goHome() {
				uni.switchTab({ url: `/pages/adopt/index` })
			}
		},
	}
</script>

<style lang="less">
.page {
	display: flex;
	flex-direction: column;
	h6 {
		margin: 20rpx 50rpx 0 50rpx;
	}
}
</style>
