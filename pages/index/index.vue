<template>
	<view>
		<view class="status_bar">
			<!-- 这里是状态栏 -->
		</view>

		<search-bar></search-bar>

		<az-swiper :imgArr="swiperImages"></az-swiper>

		<function-sort :functionSortArr="functionSortArr"></function-sort>
		
		<list-header>
			<template #title>猜你喜欢</template>
			<template #tips>更多推荐</template>
		</list-header>

	</view>
</template>

<script>
	import searchBar from '@/components/search-bar.vue';
	import azSwiper from '@/components/az-swiper.vue';
	import functionSort from '@/components/function-sort.vue';
	import listHeader from '@/components/list-header.vue';
	export default {
		components: {
			"search-bar": searchBar,
			"az-swiper": azSwiper,
			"function-sort": functionSort,
			"list-header": listHeader
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