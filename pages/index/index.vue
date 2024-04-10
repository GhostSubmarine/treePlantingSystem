<template>
	<view class="content">
		<map class="map" 
		style="width: 750rpx; height: 750rpx;" 
		:latitude="latitude" 
		:scale="scale"
		:longitude="longitude" 
		:markers="covers" />
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello',
				latitude: 40.7128,
				longitude: -74.0060,
				scale: 14,
				covers: [
					{
					  latitude: 40.7128,
					  longitude: -74.0060,
					  title: '100棵待领养',
					  iconPath: '../../static/fa5-tree-fas 1 Copy 1.svg',
					},
					{
					  latitude: 40.7128,
					  longitude: -74.0160,
					  title: '100棵待领养',
					  iconPath: '../../static/fa5-tree-fas 1 Copy 1.svg',
					},
					{
					  latitude: 40.8128,
					  longitude: -74.0060,
					  title: '100棵待领养',
					  iconPath: '../../static/fa5-tree-fas 1 Copy 1.svg',
					},
					{
					  latitude: 40.6128,
					  longitude: -74.0060,
					  title: '100棵待领养',
					  iconPath: '../../static/fa5-tree-fas 1 Copy 1.svg',
					}
				]
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style>
.page {
	width: 750rpx;
}
</style>
