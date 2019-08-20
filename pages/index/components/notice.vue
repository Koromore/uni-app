<template>
	<view class="notice">
		<view class="left">
			公告
		</view>
		<swiper class="swiper2" :indicator-dots="false" :autoplay="autoplay" :interval="interval" :duration="duration" :circular="circular" vertical="true">
			<swiper-item>
				<view class="swiper-item">
					新闻1
				</view>
			</swiper-item>
			<swiper-item>
				<view class="swiper-item">
					新闻2
				</view>
			</swiper-item>
			<swiper-item>
				<view class="swiper-item">
					新闻3
				</view>
			</swiper-item>
		</swiper>
	</view>
</template>

<script>
	export default {
		name: 'IndexNotice',
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
	/* @import url("Uni-app/uni.scss"); */
	.notice{
		width: 750upx;
		display: flex;
		flex-wrap: wrap;
		background: #FFFFFF;
	}
	
	.swiper2 {
		width: 640upx;
		height: 64upx;
	}
	
	.swiper2 swiper-item{
		width: 640rpx;
		color: red;
	}
	
	.swiper2 swiper-item view{
		line-height: 64upx;
	}
	
	.left{
		width: 110upx;
		line-height: 64upx;
	}
</style>
