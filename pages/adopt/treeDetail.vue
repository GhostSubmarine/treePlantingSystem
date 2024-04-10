<template>
	<view class="page">
		<image class="tree-img" src="../../static/adopt/图片 1@1x.png" />
		<u-list style="flex: 1;">
			<u-list-item>
				<u-cell
					:title="`编号：${treeDetail.no}`"
				>
				</u-cell>
			</u-list-item>
			<u-list-item>
				<u-cell
					:title="`种类${treeDetail.type}`"
				>
				</u-cell>
			</u-list-item>
			<u-list-item>
				<u-cell
					:title="`规格${treeDetail.size}`"
				>
				</u-cell>
			</u-list-item>
			<u-list-item>
				<u-cell
					:title="`认捐${treeDetail.user}`"
				>
				</u-cell>
			</u-list-item>
			<u-list-item>
				<u-cell
					:title="`所属${treeDetail.owner}`"
				>
				</u-cell>
			</u-list-item>
			<u-list-item>
				<u-cell
					:title="`具体位置${treeDetail.location}`"
				>
				</u-cell>
			</u-list-item>
			<u-list-item>
				<u-cell
					:title="`介绍${treeDetail.desc}`"
				>
				</u-cell>
			</u-list-item>
		</u-list>
		<u-button @click="goConfirm" type="primary" style="width: 50%; margin: 20rpx auto;" shape="circle" text="我要认养"></u-button>
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
			goConfirm() {
				uni.navigateTo({ url: `/pages/adopt/adoptConfirm` })
			}
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
}
</style>
