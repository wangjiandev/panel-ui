<template>
	<view class="content">
		<view class="map"></view>
		<panel></panel>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello'
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style lang="scss">
	page {
		height: 100%;
		display: flex;
	}

	.content {
		flex: 1;
		display: flex;
		flex-direction: column;
		width: 100vw;
		overflow: hidden;
		background-color: #E8ECF3;
		position: relative;
	}
</style>
