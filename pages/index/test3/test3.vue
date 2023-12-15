<template>
	<view>
		<view>
			<button @click="to1" type="primary">点击跳转 - test1</button>
			<button @click="to2" type="primary">点击跳转 - test2</button>
			<button @click="toindex" type="primary">点击跳转 - index</button>
			<button @click="to4()" type="primary">点击跳转 - test4</button>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			to1()
			{
				uni.switchTab({
					url:'/pages/index/test1/test1',
				})
			},
			to2()
			{
				uni.switchTab({
					url:'/pages/index/test2/test2',
				})
			},
			toindex()
			{
				uni.switchTab({
					url:'/pages/index/index',
				})
			},
			to4()
			{
				uni.navigateTo({
					url:'/pages/index/test4/test4'
				})
			},
		}
	}
</script>

<style>
button{
	margin: 5px;
}
</style>
