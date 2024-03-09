<template>
	<swiper indicator-dots autoplay circular indicator-active-color="#fff" class="swiper m-2">
		<swiper-item v-for="(item, index) in imgArr" :key="index">
			<image v-if="item.src" :src="item.src" mode="aspectFill" class="w-100"></image>
		</swiper-item>
	</swiper>
</template>

<script>
	export default {
		name: "az-swiper",
		props: {
			imgArr: {
				type: Array,
				default: []
			}
		},
	}
</script>

<style scoped>
	.swiper {
		height: 380rpx;
	}
</style>