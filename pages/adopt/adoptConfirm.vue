<template>
	<view class="page">
		<img class="tree-img" src="../../static/adopt/图片 1@1x.png" />
		<u--form
			style="margin: 20rpx;"
			labelPosition="left"
			:model="model1"
			:rules="rules"
			ref="uForm"
			labelWidth="90"
		>
			<u-form-item
				label="姓名"
				prop="userInfo.username"
				borderBottom
				ref="item1"
			>
				<u--input
					v-model="model1.userInfo.username"
					border="none"
				></u--input>
			</u-form-item>
			<u-form-item
				label="手机号"
				prop="userInfo.phone"
				borderBottom
				ref="item1"
			>
				<u--input
					v-model="model1.userInfo.phone"
					border="none"
				></u--input>
			</u-form-item>
			<u-form-item
				label="认养寄语"
				prop="userInfo.note"
				borderBottom
				ref="item1"
			>
				<u--input
					v-model="model1.userInfo.note"
					border="none"
				></u--input>
			</u-form-item>
		</u--form>
		<u-button @click="goConfirm2" type="primary" style="width: 50%; margin: 20rpx auto;" shape="circle" text="我要认养"></u-button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				model1: {
					userInfo: {
						username: 'xxx',
						phone: '18211111111',
						note: '播散一份春意，成就一份未来。'
					},
				},
				rules: {
					'userInfo.username': {
						type: 'string',
						required: true,
						message: '请填写姓名',
						trigger: ['blur', 'change']
					},
					'userInfo.phone': {
						type: 'string',
						max: 1,
						required: true,
						message: '请填写手机号',
						trigger: ['blur', 'change']
					},
				}
			};
		},
		methods: {
			goConfirm2() {
				uni.navigateTo({ url: `/pages/adopt/adoptConfirm2` })
			}
		},
		onReady() {
			//如果需要兼容微信小程序，并且校验规则中含有方法等，只能通过setRules方法设置规则。
			this.$refs.uForm.setRules(this.rules)
		},
	}
</script>

<style lang="less">
.page {
	.tree-img {
		width: 759rpx;
	}
}
</style>
