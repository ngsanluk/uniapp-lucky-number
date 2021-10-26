<template>
	<view class="content">
		<text class="luckyNumber">
			{{ luckyNumber == 0 ? "?" : luckyNumber }}
		</text>		
		<button v-on:click="play">Play</button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello',
				luckyNumber: 0
			}
		},
		onLoad() {

		},
		methods: {
			play: function() {
			  console.log("play() function called");
			  var luckyNumber = Math.floor((Math.random() * 100) + 1);
			  this.luckyNumber = luckyNumber;
			}
		}
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}
	
	.luckyNumber {
	  font-size: 900%;
	  color: #CC0000;
	  padding-top: 400rpx;
	}
</style>
