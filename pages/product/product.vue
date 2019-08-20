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
	height: 100%;
	.content
		height: 100%;
</style>
