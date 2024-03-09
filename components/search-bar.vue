<template>
	<view class="search-bar flex align-center mx-2 border rounded bg-light" :class="isMP ? 'mp-search-bar' : ''">
		<iconfont iconId="icon-tubiao11" iconSize="25" iconColor="text-light-muted" class="p-1"></iconfont>
		<input class="flex-1" :class="isMP ? 'font' : 'font-sm'" placeholder="搜索你想听的节目" />
	</view>
</template>

<script>
	export default {
		name: "search-bar",
		data() {
			return {
				isMP: this.$isMP
			}
		}
	}
</script>

<style scoped>
	.search-bar {
		opacity: 0.8;
		height: 60rpx;
	}

	.mp-search-bar {
		width: 488rpx;
		margin: 3rpx 20rpx;
	}
</style>