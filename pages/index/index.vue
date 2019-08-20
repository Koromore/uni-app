<template>
	<view class="content">
		<index-banner></index-banner>
		<index-notice></index-notice>
		<index-nav></index-nav>
		<index-advertising1></index-advertising1>
		<index-productlist></index-productlist>
		<index-advertising2></index-advertising2>
	</view>
</template>

<script>
	import IndexBanner from './components/banner.vue'
	import IndexNotice from './components/notice.vue'
	import IndexNav from './components/nav.vue'
	import IndexAdvertising1 from './components/advertising1.vue'
	import IndexProductlist from './components/productlist.vue'
	
	import IndexAdvertising2 from './components/advertising2.vue'
	export default {
		name: 'Index',
		components: {
		  IndexBanner,
			IndexNotice,
			IndexNav,
			IndexAdvertising1,
			IndexProductlist,
			IndexAdvertising2
		},
		data() {
			return {
			}
		},
		onLoad() {
			// console.log("123")
			// uni.request({
			// 	url: 'https://xcx.hmj319.cn/api/Config/getIndexConfig', //仅为示例，并非真实接口地址。
			// 	data: {
			// 		// text: 'uni.request'
			// 	},
			// 	method: 'POST',
			// 	header: {
			// 		'custom-header': 'application/json' //自定义请求头信息
			// 	},
			// 	success: (res) => {
			// 		console.log(res.data);
			// 		// this.text = 'request success';
			// 		this.banner = res.data.banner;
			// 		this.productType = res.data.proType;
			// 		this.advList = res.data.advList;
			// 		this.productList = res.data.productList;
			// 	}
			// });
		},
		methods: {

		}
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		background: #f4f4f4;
	}
</style>
