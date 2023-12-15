<template>
	<view>
		<button @click="to1" type="primary">返回</button>
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
				uni.navigateBack({
					delta:1
				})
			},
			test()
			{
				console.log("方法test被调用");
			}
		},
		onLoad() {
			var pages = getCurrentPages();
			console.log(pages);
			var page = pages[pages.length - 1];
			const vm = page.$vm;
			console.log("vm:",vm);
			// 获取页面数据
			console.log(vm.$data.title);
			// 调用页面方法
			vm.test()
		}
	}
</script>

<style>

</style>
