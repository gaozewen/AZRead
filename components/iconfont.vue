<template>
	<view class="flex align-center">
		<text class="iconfont" :class="[iconId,iconColor]" :style="{fontSize:`${iconSize}rpx`}"></text>
	</view>
</template>

<script>
	export default {
		props: {
			iconId: {
				type: String,
				default: ''
			},
			iconColor: {
				type: String,
				default: 'text-dark'
			},
			iconSize: {
				type: Number,
				default: 45
			}
		}
	}
</script>