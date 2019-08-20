<template>
	<div class="advertising" ref="advertising">
		<img class="advertising_img" src="/static/images/advertising/3.jpg" mode="widthFix" />
	</div>
</template>

<script>
	export default {
		name: 'ProductHeader',
		data() {
			return {
				advertisingHeight: '',
			}
		},
		// onShow() {
		// 	let advertisingHeight = this.$refs.advertising.offsetHeight; //100
		// 	console.log(advertisingHeight)
		// },
		mounted() {
			let advertisingHeight = this.$refs.advertising.offsetHeight; //100
			// console.log(advertisingHeight)
			this.$emit("mounted",this.advertisingHeight,true);
		}
	}
</script>

<style lang="sass" scoped>
	.advertising
		width: 750upx;
		height: 300upx;
		.advertising_img
			width: 750upx;
</style>
