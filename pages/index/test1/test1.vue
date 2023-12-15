<template>
	<view>
		<button @click="to" type="primary">点击跳转 - navigateTo</button>
		<button @click="to2" type="primary">点击跳转 - redirectTo</button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			to()
			{
				uni.navigateTo({
					url:'/pages/index/test2/test2?a=1&b=2',
				})
			},
			to2()
			{
				uni.redirectTo({
					url:'/pages/index/test2/test2?a=3&b=4',
				})
			}
		}
	}
</script>

<style>
button{
	margin: 5px;
}
</style>
