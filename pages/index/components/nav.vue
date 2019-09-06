<template>
	<div class="nav">
		<div class="nav_list"  v-for="(item, index) in productType" :key="index">
			<img class="img" :src="'/static/images/nav/'+index+'.jpg'" mode="aspectFill"/>
			<div class="nav_text">{{item.type_name}}</div>
		</div>
	</div>
</template>

<script>
	export default {
		name: 'IndexNav',
		data() {
			return {
			}
		},
		props: {
			productType: Array
		},
	}
</script>

<style lang="sass" scoped>
	.nav
		width: 750upx
		display: flex
		flex-wrap: wrap
		background: #FFFFFF
		margin-top: 24upx
		.nav_list
			width: 25%
			display: flex
			flex-wrap: wrap
			flex-direction: column
			justify-content: center
			align-content: center
			align-items: center
			margin: 24upx 0
			.img
				width: 100upx
				height: 100upx
			.nav_text
				font-size: 28upx
			
</style>
