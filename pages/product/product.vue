<template>
	<div class="content" ref="content">
		<product-header ref="header"></product-header>
		<product-seek ref="seek"></product-seek>
		<product-list :contentHeight="contentHeight"
									:headertHeight="headertHeight"
									:seekHeight="seekHeight"></product-list>
	</div>
</template>

<script>
import ProductHeader from './components/header.vue';
import ProductSeek from './components/seek.vue';
import ProductList from './components/list.vue';
export default {
	name: 'Product',
	components: {
		ProductHeader,
		ProductSeek,
		ProductList
	},
	data() {
		return {
			contentHeight: "",
			headertHeight: "",
			seekHeight: ""
		};
	},
	onLoad() {},
	mounted(data) {
		let contentHeight = this.$refs.content.offsetHeight; //100
		let headertHeight = this.$refs.header.$el.clientHeight;
		let seekHeight = this.$refs.seek.$el.clientHeight;
		// console.log(contentHeight)
		// console.log(headertHeight)
		// console.log(seekHeight)
		this.contentHeight = contentHeight
		this.headertHeight = headertHeight
		this.seekHeight = seekHeight
	},
	onLoad() {
		// console.log("123")
		uni.request({
			url: 'https://xcx.hmj319.cn/api/product/getProductList', //仅为示例，并非真实接口地址。
			data: {
				id: '9'
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
				// console.log(typeof(this.advList))
			}
		});
	},
	methods: {
		/**
		 * 点击segmentedControl 事件回调
		 */
		onClickItem(index) {
			if (this.current !== index) {
				this.current = index;
			}
		}
	}
};
</script>

<style lang="sass" scoped>
uni-page-body
	height: 100%
	.content
		height: 100%
</style>
