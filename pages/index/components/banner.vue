<template>
	<view class="banner">
		<swiper class="swiper" :indicator-dots="indicatorDots" :autoplay="autoplay" :interval="interval" :duration="duration"
		 :circular="circular">
			<swiper-item v-for="(item, index) in banner" :key="index">
				<view class="swiper-item">
					<image :src="'/static/images/banner/'+index+'.jpg'" mode="aspectFill"></image>
				</view>
			</swiper-item>
		</swiper>
	</view>

</template>

<script scoped>
	export default {
		name: 'IndexBanner',
		props: {
			banner: Array
		},
		data() {
			return {
				background: ['color1', 'color2', 'color3'],
				indicatorDots: true,
				autoplay: true,
				circular: true,
				interval: 2000,
				duration: 500,
				imgPr: "https://xcx.hmj319.cn/images/"
			}
		},
		onLoad() {
			// console.log(this.banner)
			console.log(this.background)
		},
		mounted() {
			// console.log(this.banner)
		}
	}
</script>

<style lang="sass" scoped>
	.swiper 
		width: 750upx
		height: 464upx
	// swiper-item 里面的图片高度
	swiper-item image 
		width: 100%
		height: 464upx
	
</style>
