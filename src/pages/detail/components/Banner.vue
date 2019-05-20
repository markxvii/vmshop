<template>
	<div>
		<div class="banner" @click="handleBannerClick">
			<img class="banner-img"
				 src="https://img1.qunarzz.com/p/tts3/1506/48/f6c9f836b0b712.jpg_r_640x420x90_f0ddaf13.jpg" alt="">
			<div class="banner-info">
				<div class="banner-title"></div>
				<div class="banner-number">
					<span class="iconfont banner-icon">&#xe64b;</span>
					39
				</div>
			</div>
		</div>
		<common-gallary :imgs="imgs" v-if="showGallary" @close="handleGallaryClose"></common-gallary>
	</div>
</template>

<script>
	import CommonGallary from 'common/gallary/Gallary'

	export default {
		name: "DetailBanner",
		data() {
			return {
				showGallary: false,
				imgs: ['http://img1.qunarzz.com/sight/p0/1904/34/3400fe6160c9fec4a3.img.jpg_350x240_361022d6.jpg', 'http://img1.qunarzz.com/sight/p0/1904/34/3400fe6160c9fec4a3.img.jpg_350x240_361022d6.jpg']
			}
		},
		methods: {
			handleBannerClick() {
				this.showGallary = true
			},
			handleGallaryClose() {
				this.showGallary = false
			}
		},
		components: {
			CommonGallary,
		}
	}
</script>

<style lang="stylus" scoped>
	.banner
		position: relative
		overflow hidden
		height 0
		padding-bottom 55%

		.banner-img
			width 100%

		.banner-info
			position: absolute
			left: 0
			right: 0
			bottom: 0
			line-height .6rem
			display flex
			color: #fff
			background-image: linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8))

			.banner-title
				font-size: .32rem
				flex: 1
				padding: 0 .2rem

			.banner-number
				margin-top: .14rem
				padding: 0 .4rem
				line-height: .4rem
				height: .32rem
				font-size: .24rem
				border-radius .2rem
				background: rgba(0, 0, 0, .8)

				.banner-icon
					font-size: .24rem
</style>
