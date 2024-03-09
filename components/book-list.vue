<template>
	<view :style="wrapperStyle">
		<block v-for="book in bookListArr" :key="book.id">
			<view class="flex align-center p-1 border-bottom" hover-class="bg-light" style="height: 320rpx;">
				<image :src="book.imgurl" mode="aspectFill" class="rounded mx-2" style="width: 250rpx;height: 250rpx;">
				</image>
				<view class="flex-1 pt-2" style="height: 100%;">
					<view class="py-2 font-md font-weight-bold"> {{book.name}} </view>
					<view class="font text-light-black"> {{book.synopsis}} </view>
				</view>
			</view>
		</block>
	</view>
</template>

<script>
	export default {
		name: "book-list",
		props: {
			bookListArr: {
				type: Array,
				default: []
			},
			wrapperStyle: {
				type: String,
				default: ''
			}
		}
	}
</script>