<template>
	<swiper indicator-dots autoplay circular indicator-active-color="#fff" class="swiper m-2" @change="onChangeSwiper">
		<swiper-item v-for="(item, index) in imgArr" :key="index">
			<image v-if="item.src" :src="item.src" mode="aspectFill" class="w-100 animated"
				:class="currentImgIndex === index ? 'my-animate' : ''"></image>
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
		data() {
			return {
				currentImgIndex: 0,
			}
		},
		methods: {
			onChangeSwiper(e) {
				this.currentImgIndex = e.detail.current
			}
		}
	}
</script>

<style scoped>
	.swiper {
		height: 380rpx;
	}
</style>