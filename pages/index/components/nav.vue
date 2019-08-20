<template>
	<div class="nav">
		<div class="nav_list">
			<img class="img" src="/static/images/nav/1.jpg" mode="aspectFill"/>
			<div class="nav_text">项目1</div>
		</div>
		<div class="nav_list">
			<img class="img" src="/static/images/nav/2.jpg" mode="aspectFill">
			<div class="nav_text">项目2</div>
		</div>
		<div class="nav_list">
			<img class="img" src="/static/images/nav/3.jpg" mode="aspectFill">
			<div class="nav_text">项目3</div>
		</div>
		<div class="nav_list">
			<img class="img" src="/static/images/nav/4.jpg" mode="aspectFill">
			<div class="nav_text">项目4</div>
		</div>
		<div class="nav_list">
			<img class="img" src="/static/images/nav/5.jpg" mode="aspectFill">
			<div class="nav_text">项目5</div>
		</div>
		<div class="nav_list">
			<img class="img" src="/static/images/nav/6.jpg" mode="aspectFill">
			<div class="nav_text">项目6</div>
		</div>
		<div class="nav_list">
			<img class="img" src="/static/images/nav/7.jpg" mode="aspectFill">
			<div class="nav_text">项目7</div>
		</div>
		<div class="nav_list">
			<img class="img" src="/static/images/nav/8.jpg" mode="aspectFill">
			<div class="nav_text">项目8</div>
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
	}
</script>

<style>
	.nav{
		width: 750upx;
		display: flex;
		flex-wrap: wrap;
		background: #FFFFFF;
		margin-top: 24upx;
	}
	
	.nav_list{
		width: 25%;
		display: flex;
		flex-wrap: wrap;
		flex-direction: column;
		justify-content: center;
		align-content: center;
		align-items: center;
		margin: 24upx 0;
	}
	
	.nav_list .img{
		width: 100upx;
		height: 100upx;
	}
	
	.nav_list .nav_text{
		font-size: 28upx;
	}
</style>
