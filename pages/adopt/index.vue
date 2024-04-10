<template>
	<view class="page">
		<image class="swipe-img" src="../../static/adopt/轮播图 1@1x.png" />
		<u-list>
			<u-list-item v-for="item in locationData" :key="item.id">
				<u-cell
					@click="goDetail"
					:title="`${item.location}`"
					:value="`(${item.num}株待认养)`"
					:isLink="true"
				>
				</u-cell>
			</u-list-item>
		</u-list>
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
}
</style>
