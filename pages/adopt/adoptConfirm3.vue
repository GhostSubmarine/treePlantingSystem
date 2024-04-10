<template>
	<view class="page">
		<h6>
			个人信息
		</h6>
		<u--text :text="`姓名:${info.userName}`" style="margin: 10rpx 50rpx;"></u--text>
		<u--text :text="`电话:${info.phone}`" style="margin: 10rpx 50rpx;"></u--text>
		<u--text :text="`认养寄语:${info.note}`" style="margin: 10rpx 50rpx;"></u--text>
		<h6>
			树木信息
		</h6>
		<u--text :text="`树木编号:${info.no}`" style="margin: 10rpx 50rpx;"></u--text>
		<u--text :text="`树种:${info.type}`" style="margin: 10rpx 50rpx;"></u--text>
		<u--text :text="`所属义务植树点:${info.onwer}`" style="margin: 10rpx 50rpx;"></u--text>
		<h6>
			账单信息
		</h6>
		<u--text :text="`金额:${info.money}`" style="margin: 10rpx 50rpx;"></u--text>
		<view style="display: flex;margin: 10rpx 50rpx;align-items: baseline; gap: 2rpx;">
			<u-icon name="info-circle"></u-icon>
			<text style="color: grey;">本次为单年认养费用，如需连续认养可通过“继续认养”按钮实现，提交后7个工作日可以来查看审核结果，如果审核不通过，会有工作人员联系并退款</text>
		</view>
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
					note: '播散一份绿意，成就一份未来。',
					no: 'xxxx',
					type: 'xxx',
					onwer: 'xxxx',
					money: '200'
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
@font16: 31rpx;
@font14: 27rpx;
@font18: 35rpx;
.page {
	display: flex;
	flex-direction: column;
	h6 {
		margin: 20rpx 50rpx 0 50rpx;
		font-size: @font18;
	}
}
</style>
