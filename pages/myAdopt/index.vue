<template>
	<view class="page">
		<view class="select-list">
			<u--input
				v-model="userInfo.sex"
				border="surround"
				disabled
				disabledColor="#ffffff"
				placeholder="种类"
				suffixIcon="arrow-right"
				@click="show=true"
			></u--input>
			<u--input
				v-model="userInfo.sex"
				border="surround"
				disabled
				disabledColor="#ffffff"
				placeholder="类别"
				suffixIcon="arrow-right"
				@click="show=true"
			></u--input>
			<u--input
				v-model="userInfo.sex"
				border="surround"
				disabledColor="#ffffff"
				placeholder="认养状态"
				disabled
				suffixIcon="arrow-right"
				@click="show=true"
			></u--input>
		</view>
		<List v-for="item in adoptData" :data="item" :key="item.id" />
		<u-picker :show="show" :columns="columns"></u-picker>
	</view>
</template>

<script>
	import List from '../../components/list.vue'
	export default {
		components: {
			List	
		},
		data() {
			return {
				adoptData: [
					{status: 1, id: '1', no: 'xxxxxx', type: 'xxx', user: 'xxxx'},
					{status: 2, id: '2', no: 'xxxxxx', type: 'xxx', user: 'xxxx'},
					{status: 3, id: '3', no: 'xxxxxx', type: 'xxx', user: 'xxxx'},
					{status: 1, id: '4', no: 'xxxxxx', type: 'xxx', user: 'xxxx'},
					{status: 2, id: '5', no: 'xxxxxx', type: 'xxx', user: 'xxxx'},
					{status: 3, id: '6', no: 'xxxxxx', type: 'xxx', user: 'xxxx'}
				],
				columns: [
					['中国', '中国', '中国']
				],
				show: false,
				userInfo: {
					sex: ''
				}
			};
		},
		methods: {
			confirm(e) {
				console.log(e);
			}
		}
	}
</script>

<style lang="less">
.page {
	.select-list {
		display: flex;
		align-self: center;
		gap: 20rpx;
		padding: 20rpx 20rpx;
	}
}
</style>
