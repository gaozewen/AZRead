<template>
	<view>
		<view class="status_bar">
			<!-- 这里是状态栏 -->
		</view>
		<!-- <view :style="{height:`${statusBarHeight}px`,background:'pink'}"></view> -->
		<view>{{statusBarHeight}}</view>
	</view>
</template>

<script>
	const statusBarHeight = uni.getSystemInfoSync().statusBarHeight

	export default {
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