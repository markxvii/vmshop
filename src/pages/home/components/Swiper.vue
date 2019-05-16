<template>
	<div class="wrapper">
		<swiper :options="swiperOption" ref="mySwiper" @someSwiperEvent="callback">
			<swiper-slide v-for="item of swiperList" :key="item.id"><img class="swiper-img" :src="item.imgUrl"
							   alt=""></swiper-slide>
			<div class="swiper-pagination" slot="pagination"></div>
		</swiper>
	</div>
</template>

<script>
	export default {
		name: "HomeSwiper",
		data() {
			return {
				swiperOption: {
					pagination:'.swiper-pagination',
					loop:true,
				},
				swiperList:[{
					id:'0001',
					imgUrl:"//c3.xinstatic.com//c/20190128/1516/5c4eac64729c7945932.png"
				},{
					id:'0002',
					imgUrl:"//c3.xinstatic.com//c/20181010/1903/5bbddc6beefcb701176.png"
				}]
			}
		}
	}
</script>

<style lang="stylus" scoped>
	.wrapper >>> .swiper-pagination-bullet-active
		background red !important

	.wrapper
		overflow:hidden
		width 100%
		height 0
		padding-bottom 42.67%
		.swiper-img
			width 100%

</style>
