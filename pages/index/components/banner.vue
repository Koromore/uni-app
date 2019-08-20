<template>
	<view class="banner">
		<swiper class="swiper" :indicator-dots="indicatorDots" :autoplay="autoplay" :interval="interval" :duration="duration"
		 :circular="circular">
			<swiper-item>
				<view class="swiper-item">
					<image src="/static/images/banner/1.jpg" mode="aspectFill"></image>
				</view>
			</swiper-item>
			<swiper-item>
				<view class="swiper-item">
					<image src="/static/images/banner/2.jpg" mode="aspectFill"></image>
				</view>
			</swiper-item>
			<swiper-item>
				<view class="swiper-item">
					<image src="/static/images/banner/3.jpg" mode="aspectFill"></image>
				</view>
			</swiper-item>
			<swiper-item>
				<view class="swiper-item">
					<image src="/static/images/banner/4.jpg" mode="aspectFill"></image>
				</view>
			</swiper-item>
		</swiper>
	</view>

</template>

<script>
	export default {
		name: 'IndexBanner',
		data() {
			return {
				background: ['color1', 'color2', 'color3'],
				indicatorDots: true,
				autoplay: true,
				circular: true,
				interval: 2000,
				duration: 500
			}
		},
	}
</script>

<style>
	.swiper {
		width: 750upx;
		height: 464upx;
	}

	.notice {
		width: 750upx;
		height: 64upx;
		display: flex;
		flex-wrap: wrap;

	}

	.left {
		width: 110upx;
		line-height: 64upx;
	}

	// swiper-item 里面的图片高度
	swiper-item image {
		width: 100%;
		height: 464upx;
	}
</style>
