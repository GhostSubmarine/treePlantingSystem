<template>
	<view class="page">
		<!-- <u--text text="协议内容" style="margin: 20rpx;"></u--text> -->
		<h1>常州市城市绿地（树木）认种认养协议书</h1>
		<u--textarea v-model="value" autoHeight style="margin: 0 20rpx;" border="none" disabled>
			
		</u--textarea>
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
				value: `
		城市绿地(树木)认种认养，是指通过直接投工投劳或者捐资代劳，在指定地点新建乔、灌、草植被，或者对指定乔、灌、草植被进行冠名或者非冠名养护的全民义务植树尽责形式之一。
		为深入开展全民义务植树活动，积极倡导全社会参与绿色公益事业，巩固绿化成果，改善生态环境。根据《城市绿地认种认养实施办法》(常绿办(2005〕3号):本着自愿认养、互相监督的原则，签订绿地(树木)认种认养协议书如下:
		一、甲方:青枫公园
			乙方:xxxx
		二、乙方自愿捐资200元人民币。
		三、乙方认种认养的绿地(树木)的为:
			编号:QFGYPTSMHF0003
			种类:红枫
			元人江"L
			具体位置:null
			四、认种认养期限
				2024年4月10日至2025年4月10日
			五、甲方按照有关园林绿化养护管理技术标准实施认种认养绿地(树木)的管护;按照《市区古树名木保护管理办法》实施认养古树的保护管理。
			六、双方的权利和责任:
			1.甲方对认种认养者颁发认种认养证书。
			2.甲方十五个工作日内设置认养牌。
			3.认种认养不改变绿地(树木)产权关系。
			4.认种认养期间，双方互相监督:若甲方未按双方的协议执行，乙方可提出异议，否则，乙方不再提供资金并可要求返还已提供的资金;乙方未按规定要求进行认种认养，甲方可提出期限整改，否则可摘除认养牌
			甲方:青枫公园
			乙方:xxxx`
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
	@font18: 35rpx;
.page {
	display: flex;
	flex-direction: column;
	h1 {
		font-size: @font18;
		margin: 10rpx auto;
	}
}
</style>
