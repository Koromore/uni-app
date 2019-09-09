<template>
	<div class="advertising">
		<image class="advertising_img" :src="imgPr + advList[0].img" mode="widthFix" /></image>
	</div>
</template>

<script>
	export default {
		name: 'IndexAdvertising',
		data() {
			return {
				imgPr: 'https://xcx.hmj319.cn/upload/'
			}
		},
		props: {
			advList: Object
		},
		methods: {
			
		},
		mounted() {
			console.log(this.advList)
		}
	}
</script>

<style lang="sass" scoped>
	.advertising
		width: 750upx
		margin-top: 24upx
		.advertising_img
			width: 750upx
</style>
