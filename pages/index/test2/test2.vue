<template>
	<view>
		<h1>a={{a}}</h1>
		<h1>b={{b}}</h1>
		<view>
			<button @click="to3" type="primary">点击跳转 - reLaunch</button>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				a:'',
				b:''
			}
		},
		methods: {
			to3()
			{
				uni.reLaunch({
					url:'/pages/index/index'
				})
			}
		},
		onLoad(option) {
			this.a=option.a;
			this.b=option.b;
		}
	}
</script>

<style>

</style>
