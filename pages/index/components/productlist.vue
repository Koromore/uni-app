<template>
	<div class="product_list">
		<div class="title">精品推荐</div>
		<div class="product_box">
			<div class="product" v-for="(item, index) in productList" :key="index">
				<img class="img" :src="imgPr + item.img[0]" mode="widthFix"/>
				<div class="text">产品名称</div>
			</div>
		</div>
		<div class="more">
			<div class="more_text">更多</div>
		</div>
	</div>
</template>

<script>
	export default {
		name: 'IndexProductlist',
		data() {
			return {
				imgPr: 'https://xcx.hmj319.cn/upload/'
			}
		},
		props: {
			productList: Array
		},
	}
</script>

<style lang="sass" scoped>
	.product_list
		width: 750upx
	.title
		width: 750upx
		height: 100upx
		text-align: center
		line-height: 100upx
		font-size: 28upx
		background: #FFFFFF url(http://hmj.cnyun365.com/static/img/title_bg.png) center center no-repeat
		background-size: 200upx
		margin-top: 24upx
	.product_box
		width: 750upx
		display: flex
		flex-wrap: wrap
		.product
			width: 48%
			box-sizing: border-box
			padding: 18upx
			margin: 1%
			background: #FFFFFF
			.img
				width: 100%
			.text
				text-align: center
				font-size: 28upx
	.more
		width: 750upx
		height: 100upx
		background: #FFFFFF
		display: flex
		flex-wrap: wrap
		justify-content: center
		align-items: center
		.more_text
			width: 180upx
			height: 60upx
			color: #FFFFFF
			text-align: center
			background: #8b562a
			border-radius: 16rpx
			font-size: 28upx
			line-height: 60upx
</style>
