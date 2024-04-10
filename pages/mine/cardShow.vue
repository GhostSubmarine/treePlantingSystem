<template>
	<view class="page">
		<h1>证书展示</h1>
		<img class="card-img" src="../../static/adopt/图片 1@1x.png" />
		<img class="card-img" src="../../static/adopt/图片 1@1x.png" />
		<img class="card-img" src="../../static/adopt/图片 1@1x.png" />
		<img class="card-img" src="../../static/adopt/图片 1@1x.png" />
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			};
		}
	}
</script>

<style lang="less">
@font16: 31rpx;
@font14: 27rpx;
@font18: 35rpx;
.page {
	display: flex;
	flex-direction: column;
	gap: 50rpx;
	.card-img {
		width: 65%;
		margin: 0 auto;
	}
	h1 {
		font-size: @font18;
		margin: 20rpx auto;
	}
}
</style>
