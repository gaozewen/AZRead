<template>
	<view>
		<list-header>
			<template #title>猜你喜欢</template>
			<template #tips>更多推荐</template>
		</list-header>

		<view class="flex">
			<block v-for="(item, index) in recommedBooks" :key="index">
				<view class="flex flex-column align-center flex-1 position-relative">
					<image :src="item.src" mode="widthFix" class="w-100"></image>
					<text class="font my-1 text-light-black">{{item.name}}</text>
					<iconfont iconId="icon-erji" iconSize="35" iconColor="text-light-white" class="position-absolute"
						style="left: 54rpx; top: 20rpx;"></iconfont>
				</view>
			</block>
		</view>
	</view>
</template>

<script>
	import listHeader from '@/components/list-header.vue';
	export default {
		props: {
			recommedBooks: {
				type: Array,
				default: []
			}
		},
		components: {
			"list-header": listHeader
		},
	}
</script>

<style>
</style>