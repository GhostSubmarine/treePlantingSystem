<template>
	<view class="page">
		<image class="tree-img" src="../../static/adopt/图片 1@1x.png" />
		<view class="list">
			<text>编号：{{treeDetail.no}}</text>
			<text>种类：{{treeDetail.type}}</text>
			<text>规格：{{treeDetail.size}}</text>
			<text>认捐：{{treeDetail.user}}</text>
			<text>所属：{{treeDetail.owner}}</text>
			<text>具体位置：{{treeDetail.location}}</text>
			<text>介绍：{{treeDetail.desc}}</text>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				treeDetail: {
					no: 'xxxxxx',
					type: 'xxxxx',
					size: 'xxxxx',
					user: 'xxxx',
					owner: 'xxxx',
					location: 'xxxxxxxxxx',
					desc: 'xxxxxx'
				}
			}
		},
		methods: {
			
		}
	}
</script>

<style lang="less">
@font14: 27rpx;
.page {
	display: flex;
	flex-direction: column;
	.tree-img {
		width: 384.61rpx;
		height: 255.77rpx;
		margin: 25rpx auto;
	}
	.list {
		width: 355.77rpx;
		display: flex;
		flex-direction: column;
		gap: 20rpx;
		margin-left: 198rpx;
		color: rgba(155,155,155,1);
		font-size: @font14;
	}
}
</style>
