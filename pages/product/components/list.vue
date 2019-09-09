<template>
	<div class="list" v-bind:style="{ height: contentHeight - headertHeight - seekHeight + 'px' }">
		<div class="title_box">
			<div
				v-for="(item, index) in titlelist"
				:key="index"
				:class="currentTab == index ? 'title activ' : 'title'"
				:data-current="index"
				@click="current($event)">
				项目{{ item }}
			</div>
		</div>
		<div class="list_box">
			<swiper
				class="swiper"
				:indicator-dots="indicatorDots"
				:autoplay="autoplay"
				:interval="interval"
				:duration="duration"
				:circular="circular"
				:current="currentTab"
				@change="test"
			>
				<swiper-item v-for="(item, index) in titlelist" :key="index" class="swiper-item">
					<view>{{ item }}</view>
				</swiper-item>
			</swiper>
		</div>
	</div>
</template>

<script>
export default {
	name: 'ProductList',
	props: {
		contentHeight: '',
		headertHeight: '',
		seekHeight: ''
	},
	data() {
		return {
			// background: ['color1', 'color2', 'color3'],
			indicatorDots: false,
			autoplay: false,
			circular: true,
			interval: 2000,
			duration: 500,
			currentTab: 0,
			height: 100,
			titlelist: [1, 2, 3, 4, 5, 6]
		};
	},
	methods: {
		current(e) {
			this.currentTab = e.currentTarget.dataset.current;
			console.log(e.currentTarget.dataset.current)
		},
		test(e) {
			// console.log(e.detail.current);
			this.currentTab = e.detail.current;
			console.log(e.detail.current)
		}
	},
	// onShow() {
	// 	let contentHeight = this.contentHeight
	// 	let headertHeight = this.headertHeight
	// 	let seekHeight = this.seekHeight
	// 	let listHeight = contentHeight - headertHeight - seekHeight
	// 	console.log(contentHeight)
	// 	console.log(headertHeight)
	// 	console.log(seekHeight)
	// 	console.log(listHeight)
	// },
	mounted() {
		/* 请求数据放在这个里面 操作数据 必须记住 mounted*/
		// console.log('实例已编译');
		// var h = document.documentElement.clientHeight || document.body.clientHeight;
		// console.log('h');
	}
};
</script>

<style lang="sass" scoped>
.list
	width: 750upx
	display: flex
	flex-wrap: wrap
	.title_box
		width: 187.5upx
		display: flex
		flex-wrap: wrap
		.title
			width: 100%
			height: 81upx
			line-height: 81upx
			font-size: 30upx
			text-align: center
		.activ
			background: red
	.list_box
		width: 562.5upx
		background: red
		.swiper
			height: 100%
			.swiper-item
				height: 100%
				background: blue
</style>
