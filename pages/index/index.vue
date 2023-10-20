<template>
	<div class="color-blue"></div>
	<div class="color-pink"></div>
	<div class="color-white"></div>
	<div class="color-pink"></div>
	<div class="color-blue"></div>
</template>

<script>
	export default {
		data() {
			return {};
		},
		onLoad() {
			uni.getSystemInfo({ 
			      success: (res) => {			        
					var windowWeight= res.windowHeight;
					var windowWidth= res.windowWidth;
					console.log(windowWidth);
					console.log(windowWeight);
			      }
			    })
		},
		methods: {
			pxToRpx(px) {
			  const screenWidth = uni.getSystemInfoSync().screenWidth
			  return (750 * Number.parseInt(px)) / screenWidth
			}
		}
	}

</script>

<style>
	.uni-page-head{
	      display:none;
	  }
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
	.color-blue{
	    height: 20vh;
		weight: 100vw;
	    background-color: #cff1fe;
	}
	.color-pink{
	    height: 20vh;
		weight: 100vw;
	    background-color: #fce6eb;
	}
	.color-white{
	    height: 20vh;
		weight: 100vw;
	    background-color: #ffffff;
	}
</style>
