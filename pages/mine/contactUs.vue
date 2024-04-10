<template>
	<view>
		<u-list>
			<u-list-item>
				<u-cell
					:title="`联系电话:${info.phone}`"
				>
				</u-cell>
			</u-list-item>
			<u-list-item>
				<u-cell
					:title="`邮箱:${info.email}`"
				>
				</u-cell>
			</u-list-item>
		</u-list>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				info: {
					phone: '12312312312123',
					email: '1072727282@11.com'
				}
			};
		}
	}
</script>

<style lang="less">

</style>
