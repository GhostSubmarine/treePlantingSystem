<template>
	<view class="page">
		<List v-for="item in adoptData" :data="item" :key="item.id" />
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
				]
			};
		}
	}
</script>

<style lang="less">
.page {
	
}
</style>
