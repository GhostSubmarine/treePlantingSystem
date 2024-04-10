<template>
	<view class="container" @click="goTreeDetail">
		<view class="top">
			<!-- <text class="tree-name"></text> -->
			<u--text :text="'xx树木'"></u--text>
			<!-- <text class="status-btn" :class="{
				wait: treeObj.status === 1,
				expire: treeObj.status === 2,
				on: treeObj.status === 3
			}">{{treeObj.status | statusFilter}}</text> -->
			<u-tag :text="statusFilter(treeObj.status)" :type="typeFilter(treeObj.status)" shape="circle" />
		</view>
		<view class="bottom">
			<image class="tree-img" src="../static/adopt/图片 2 LorJGxr@1x.png" />
			<view class="tree-detail">
				<text>编号：{{treeObj.no}}</text>
				<text>种类：{{treeObj.type}}</text>
				<text>认捐：{{treeObj.user}}</text>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		name:"list",
		props: {
			data: {
				type: Object,
				default: () => ({})
			}
		},
		data() {
			return {
				treeObj: this.data
			};
		},
		methods: {
			goTreeDetail() {
				if (!this.treeObj.edit) return
				uni.navigateTo({ url: `/pages/adopt/treeDetail` })
			},
			statusFilter(status) {
				switch(status) {
					case 1:
						return '待认养'
					case 2:
						return '已过期'
					case 3:
						return '认养中'
					default:
						return ''
				}
			},
			typeFilter(status) {
				switch(status) {
					case 1:
						return 'info'
					case 2:
						return 'error'
					case 3:
						return 'success'
					default:
						return ''
				}
			}
		}
	}
</script>

<style lang="less">
@font14: 27rpx;
@font15: 29rpx;
.container {
	height: 300rpx;
	margin: 0 42.3rpx;
	padding: 0 28.85rpx 28.85rpx 28.85rpx;
	display: flex;
	flex-direction: column;
	.top {
		height: 98rpx;
		display: flex;
		align-items: center;
		justify-content: space-between;
		.tree-name {
			color: rgba(16,16,16,1);
			font-size: @font15;
		}
		.status-btn {
			width: 111.54rpx;
			height: 61.54rpx;
			border-radius: 31rpx;
			font-size: @font14;
			text-align: center;
			line-height: 61.54rpx;
			color: rgba(255, 255, 255, 1);
			&.wait {
				background-color: rgba(129,179,55,1);
			}
			&.on {
				background-color: rgba(190,190,190,1);
			}
			&.expire {
				background-color: rgba(129,179,55,1);
			}
		}
		
	}
	.bottom {
		flex: 1;
		display: flex;
		gap: 19.23rpx;
		.tree-img {
			width: 230.77rpx;
			height: 100%;
		}
		.tree-detail {
			flex: 1;
			display: flex;
			gap: 20rpx;
			flex-direction: column;
			color: rgba(155,155,155,1);
			font-size: @font14;
		}
	}
}
</style>