<template>
	<view>
		<view class="status_bar">
			<!-- 这里是状态栏 -->
		</view>
		<!-- <view :style="{height:`${statusBarHeight}px`,background:'pink'}"></view> -->
		<view>{{statusBarHeight}}</view>
		<text class="iconfont icon-shoucang font-md"></text>
		<iconfont iconId="icon-bofangsanjiaoxing"></iconfont>
	</view>
</template>

<script>
	import iconfont from '@/components/iconfont/iconfont.vue';
	const statusBarHeight = uni.getSystemInfoSync().statusBarHeight

	export default {
		components: {
			iconfont
		},
		data() {
			return {
				statusBarHeight
			}
		},
		onLoad() {

		},
		methods: {}
	}
</script>

<style>
	.status_bar {
		height: var(--status-bar-height);
		width: 100%;
		background-color: royalblue;
	}
</style>