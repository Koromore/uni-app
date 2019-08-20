<template>
	<div class="seek" ref="seek">
		<input placeholder="搜索内容" class="input" />
		<div class="sousuo">搜索</div>
	</div>
</template>

<script>
export default {
	name: 'ProductSeek',
	data() {
		return {};
	},
	mounted() {
		let seekHeight = this.$refs.seek.offsetHeight; //100
		// console.log(seekHeight)
	}
};
</script>

<style lang="sass" scoped>
	.seek
		width: 750upx;
		display: flex;
		flex-wrap: wrap;
		justify-content: center;
		align-items: center;
		.input
			width: 560upx;
			height: 60upx;
			border: 2upx solid #AAAAAA;
			border-radius: 9upx;
			font-size: 28upx;
		.sousuo
			width: 108upx;
			height: 60upx;
			margin-left: 6upx;
			line-height: 60upx;
			font-size: 28upx;
			text-align: center;
			color: red;
			border: 2upx solid red;
			border-radius: 9upx;
</style>
