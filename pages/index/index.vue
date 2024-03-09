<template>
	<view>
		<view class="status_bar">
			<!-- 这里是状态栏 -->
		</view>

		<search-bar></search-bar>

		<az-swiper :imgArr="swiperImages"></az-swiper>
		
	</view>
</template>

<script>
	import searchBar from '@/components/search-bar.vue';
	import azSwiper from '@/components/az-swiper.vue';
	export default {
		components: {
			"search-bar": searchBar,
			"az-swiper": azSwiper
		},
		data() {
			return {
				swiperImages: [1, 2, 3, 4].map(i => ({
					src: `/static/swiperImages/swipertab${i}.png`
				}))
			}
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