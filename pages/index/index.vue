<template>
	<view>
		<view class="status_bar">
			<!-- 这里是状态栏 -->
		</view>

		<search-bar></search-bar>

	</view>
</template>

<script>
	import searchBar from '@/components/search-bar.vue';
	export default {
		components: {
			"search-bar": searchBar
		},
		data() {
			
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style scoped>
	.status_bar {
		height: var(--status-bar-height);
		width: 100%;
	}

	
</style>