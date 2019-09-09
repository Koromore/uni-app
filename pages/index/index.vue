<template>
	<view class="content">
		<index-banner :banner='banner'></index-banner>
		<index-notice></index-notice>
		<index-nav :productType='productType'></index-nav>
		<index-advertising :advList='advList[1]'></index-advertising>
		<index-productlist :productList='productList'></index-productlist>
		<index-advertising :advList='advList[2]'></index-advertising>
	</view>
</template>

<script>
	import IndexBanner from './components/banner.vue'
	import IndexNotice from './components/notice.vue'
	import IndexNav from './components/nav.vue'
	import IndexAdvertising from './components/advertising.vue'
	import IndexProductlist from './components/productlist.vue'

	export default {
		name: 'Index',
		components: {
			IndexBanner,
			IndexNotice,
			IndexNav,
			IndexAdvertising,
			IndexProductlist
		},
		data() {
			return {
				banner: [],
				productType: [],
				productList: [],
				advList: {}
			}
		},
		onLoad() {
			// console.log("123")
			uni.request({
				url: 'https://xcx.hmj319.cn/api/Config/getIndexConfig', //仅为示例，并非真实接口地址。
				data: {
					// text: 'uni.request'
				},
				method: 'POST',
				header: {
					'custom-header': 'application/json' //自定义请求头信息
				},
				success: (res) => {
					// console.log(res.data)
					// this.text = 'request success'
					this.banner = res.data.banner
					this.productType = res.data.proType
					this.advList = res.data.advList
					this.productList = res.data.productList
					// console.log(this.banner)
					// console.log(this.text)
					console.log(typeof(this.advList))
				}
			});
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
