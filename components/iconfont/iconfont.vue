<template>
	<text class="iconfont" :class="[iconId,iconColor]" :style="{fontSize:iconSize}"></text>
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
