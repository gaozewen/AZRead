<template>
	<view>
		<view class="status_bar">
			<!-- 这里是状态栏 -->
		</view>

		<search-bar></search-bar>

		<az-swiper :imgArr="swiperImages"></az-swiper>

		<function-sort :functionSortArr="functionSortArr"></function-sort>

	</view>
</template>

<script>
	import searchBar from '@/components/search-bar.vue';
	import azSwiper from '@/components/az-swiper.vue';
	import functionSort from '@/components/function-sort.vue'
	export default {
		components: {
			"search-bar": searchBar,
			"az-swiper": azSwiper,
			"function-sort": functionSort
		},
		data() {
			return {
				swiperImages: [1, 2, 3, 4].map(i => ({
					src: `/static/swiperImages/swipertab${i}.png`
				})),
				functionSortArr: [{
						iconId: 'icon-icon-test',
						iconColor: 'text-warning',
						name: '看榜单'
					},
					{
						iconId: 'icon-startRead',
						iconColor: 'text-hover-primary',
						name: '听小说'
					},
					{
						iconId: 'icon-icon09',
						iconColor: 'text-light-black',
						name: '听音乐'
					},
					{
						iconId: 'icon-zhishi',
						iconColor: 'text-success',
						name: '听知识'
					}
				]
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