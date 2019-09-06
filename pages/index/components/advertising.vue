<template>
	<div class="advertising">
		<img class="advertising_img" :src="advertisingImg" mode="widthFix" />
	</div>
</template>

<script>
	export default {
		name: 'IndexAdvertising1',
		data() {
			return {
			}
		},
		props: {
			advertisingImg: String
		},
	}
</script>

<style lang="sass" scoped>
	.advertising
		width: 750upx
		margin-top: 24upx
		.advertising_img
			width: 750upx
</style>
