<template>
	<div class="wrapper">
		<swiper :options="swiperOption" ref="mySwiper" @someSwiperEvent="callback" v-if="showSwiper">
			<swiper-slide v-for="item of list" :key="item.id"><img class="swiper-img" :src="item.imgUrl"
							   alt=""></swiper-slide>
			<div class="swiper-pagination" slot="pagination"></div>
		</swiper>
	</div>
</template>

<script>
	export default {
		name: "HomeSwiper",
		props: {
			list: Array,
		},
		computed: {
			showSwiper() {
				return this.list.length
			}
		},
		data() {
			return {
				swiperOption: {
					pagination:'.swiper-pagination',
					loop:true,
				},
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
