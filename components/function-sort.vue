<template>
	<view class="flex align-center justify-between mx-3 my-4">
		<block v-for="(item,index) in functionSortArr" :key="index">
			<view class="flex flex-column align-center">
				<iconfont :iconId="item.iconId" :iconColor="item.iconColor" :iconSize="65"></iconfont>
				<text class="mt-1 font text-light-black">{{item.name}}</text>
			</view>
		</block>
	</view>
</template>

<script>
	export default {
		name: "function-sort",
		props: {
			functionSortArr: {
				type: Array,
				default: () => []
			},
		},
	}
</script>

<style>

</style>