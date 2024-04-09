<template>
	<view class="page">
		<image class="swipe-img" src="../../static/adopt/轮播图 1@1x.png" />
		<view class="row" v-for="item in locationData">
			<text class="location">{{item.location}}</text>
			<view class="row-right" @click="goDetail">
				<text>({{item.num}}株待认养)</text>
				<image class="arrow-img" src="../../static/adopt/图标 pQ1xiTP@1x.png" />
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				locationData: [{
					location: 'xx公园',
					id: '1',
					num: 10
				},{
					location: 'xx公园',
					id: '2',
					num: 10
				},{
					location: 'xx公园',
					id: '3',
					num: 10
				},{
					location: 'xx公园',
					id: '4',
					num: 10
				}]
			};
		},
		methods: {
			goDetail() {
				uni.navigateTo({ url: `/pages/adopt/detail` })
			}
		}
	}
</script>

<style lang="less">
.page {
	display: flex;
	flex-direction: column;
	.swipe-img {
		width: 721.15rpx;
		height: 384.62rpx;
		margin: 31rpx auto;
	}
	.row {
		height: 96.15rpx;
		border: 1rpx solid rgba(229,229,229,1);
		padding: 0 31rpx;
		display: flex;
		align-items: center;
		font-size: 33rpx;
		justify-content: space-between;
		.location {
			color: black;
		}
		.row-right {
			display: flex;
			gap: 40rpx;
			align-items: center;
			color: rgba(136,136,136,1);
			.arrow-img {
				height: 25rpx;
				width: 16rpx;
			}
		}
	}
}
</style>
