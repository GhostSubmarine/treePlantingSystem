<template>
	<view class="page">
		<u--text text="协议内容" style="margin: 20rpx;"></u--text>
		<u-checkbox-group
			style="margin: 20rpx auto;"
			v-model="checkboxValue1"
			placement="column"
		>
			<u-checkbox
				:customStyle="{marginBottom: '8px'}"
				v-for="(item, index) in checkboxList1"
				:key="index"
				:label="item.name"
				:name="item.name"
			>
			</u-checkbox>
		</u-checkbox-group>
		<u-button @click="goConfirm3" type="primary" style="width: 50%; margin: 20rpx auto;" shape="circle" text="我要认养"></u-button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				value1: '',
				checkboxValue1:[],
				            // 基本案列数据
				checkboxList1: [{
					name: '我已阅读并同意信息',
					disabled: false
				}],
			};
		},
		methods: {
			goConfirm3() {
				uni.navigateTo({ url: `/pages/adopt/adoptConfirm3` })
			}
		},
	}
</script>

<style lang="less">
.page {
	display: flex;
	flex-direction: column;
}
</style>
