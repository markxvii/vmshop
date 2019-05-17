<template>
	<div>
		<div class="title">特价推荐</div>
		<ul>
			<li class="item border-bottom" v-for="item of recommendList" :key="item.id">
				<div class="item-img-wrapper">
					<img class="item-img"
						 :src="item.imgUrl"
						 alt="">
				</div>
				<div class="item-info">
					<p class="item-title">{{item.title}}</p>
					<p class="item-desc">{{item.desc}}</p>
				</div>
			</li>
		</ul>
	</div>
</template>

<script>
	export default {
		name: "HomeWeekend",
		data() {
			return {
				recommendList: [
					{
						id: '0001',
						imgUrl: 'https://img1.qunarzz.com/vs_ceph_vs_tts/4051abb5-37db-43ec-aaf6-364770ad6dfb.jpg_r_1280x840x90_8e63e920.jpg',
						title: '斯文这下牛逼了',
						desc: '攻击力是现在的两倍'
					},
					{
						id: '0002',
						imgUrl: 'https://img1.qunarzz.com/vs_ceph_vs_tts/4051abb5-37db-43ec-aaf6-364770ad6dfb.jpg_r_1280x840x90_8e63e920.jpg',
						title: '斯文这下牛逼了',
						desc: '攻击力是现在的两倍'
					},
					{
						id: '0003',
						imgUrl: 'https://img1.qunarzz.com/vs_ceph_vs_tts/4051abb5-37db-43ec-aaf6-364770ad6dfb.jpg_r_1280x840x90_8e63e920.jpg',
						title: '斯文这下牛逼了',
						desc: '攻击力是现在的两倍'
					},
				]
			}
		}
	}
</script>

<style lang="stylus" scoped>
	@import '~styles/mixins.styl'
	.title
		margin-top .2rem
		line-height: .4rem
		background #eee
		text-indent .2rem

	.item-img-wrapper
		overflow hidden
		height 0
		padding-bottom 50%
		.item-img
			width 100%

	.item-info
		padding .1rem

		.item-title
			line-height .54rem
			font-size .32rem
			ellipsis()

		.item-desc
			line-height .4rem
			color: #ccc
			ellipsis()

</style>
