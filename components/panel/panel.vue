<template>
	<view class="panel" 
		@touchmove="touchmoveHandle" 
		@touchstart="touchstartHandle" 
		@touchend="touchendHandle"
		:style="{height: `${height}rpx`}"
		>
		<view class="search_wrapper">
			<view class="search_content">
				<view class="search_content_input">
					<uni-icons class="search_icon" type="search" size="22" color="#394353"></uni-icons>
					<text class="search_text">请输入搜索内容</text>
				</view>
				<image class="search_suffix" src="/static/audio.png" mode="aspectFill"></image>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				minHeight: 320,
				middleHeight: 800,
				maxHeight: 1259,
				height: 320,
				lastY: 0,
				up: true,
				direction_flag: true
			};
		},
		methods: {
			touchstartHandle(e){
				this.lastY = event.touches[0].pageY;
				// console.log('START:', this.lastY)
			},
			touchendHandle(e){
				if(this.up){
					if(this.height < this.middleHeight){
						this.height = this.middleHeight
					} else {
						this.height = this.maxHeight
					}
				} else {
					if(this.height < this.middleHeight){
						this.height = this.minHeight
					} else {
						this.height = this.middleHeight
					}
				}
				this.direction_flag = true
			},
			touchmoveHandle(e){
				let currentY = event.touches[0].pageY
				let transformHeight = currentY - this.lastY
				this.height = this.height - (transformHeight / 10)
				// if(this.height > this.maxHeight){
				// 	this.height = this.maxHeight
				// }
				// if(this.height < this.minHeight){
				// 	this.height = this.minHeight
				// }
				if(this.direction_flag){
					this.direction_flag = false
					if(transformHeight > 0){
						// 下滑
						this.up = false
					} else {
						// 上滑
						this.up = true
					}
				}
				
			}
		}
	}
</script>

<style lang="scss">
.panel{
	z-index: 999;
	position: absolute;
	bottom: 0;
	width: 100vw;
	background-color: #ffffff;
	border-radius: 20rpx 20rpx 0 0;
	padding: 30rpx 20rpx;
	box-sizing: border-box;
	box-shadow: 0 -8rpx 30rpx rgba(0, 0, 0, 0.1);
	.search_wrapper{
		display: flex;
		justify-content: center;
		align-items: center;
		.search_content{
			height: 74rpx;
			width: 100%;
			display: flex;
			justify-content: space-between;
			align-items: center;
			background-color: #EBF0F3;
			border-radius: 16rpx;
			border: 1rpx solid #DFE4E7;
			padding: 0 20rpx;
			.search_content_input{
				flex: 1;
				display: flex;
				justify-content: flex-start;
				align-items: center;
				.search_icon{
					margin-right: 10rpx;
				}
				.search_text{
					color: #595E5F;
					font-size: 32rpx;
					letter-spacing: 1.8rpx;
				}
			}
			.search_suffix{
				width: 48rpx;
				height: 48rpx;
				image{
					width: 100%;
					height: 100%;
				}
			}
		}
	}
}
</style>
