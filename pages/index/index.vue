<template>
	<view class="content">
		<map class="map" style="width: 750rpx; height: 750rpx;" :latitude="latitude" :longitude="longitude" :markers="covers" />
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello',
				latitude: '',
				longitude: '',
				covers: []
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
