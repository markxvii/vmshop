<template>
	<div>
		<div class="title">查看详情</div>
		<ul>
			<li class="item border-bottom" v-for="item of recommendList" :key="item.id">
				<img class="item-img"
					 :src="item.imgUrl"
					 alt="">
				<div class="item-info">
					<p class="item-title">{{item.title}}</p>
					<p class="item-desc">{{item.desc}}</p>
					<button class="item-button">查看详情</button>
				</div>
			</li>
		</ul>
	</div>
</template>

<script>
	export default {
		name: "HomeRecommend",
		data() {
			return {
				recommendList: [
					{id:'0001',imgUrl:'https://img1.qunarzz.com/p/tts3/1603/6e/649f8db09ea57bf7.jpg_r_240x160x90_02a57254.jpg',title:'斯文这下牛逼了',desc:'攻击力是现在的两倍'},
					{id:'0002',imgUrl:'https://img1.qunarzz.com/p/tts3/1603/6e/649f8db09ea57bf7.jpg_r_240x160x90_02a57254.jpg',title:'斯文这下牛逼了',desc:'攻击力是现在的两倍'},
					{id:'0003',imgUrl:'https://img1.qunarzz.com/p/tts3/1603/6e/649f8db09ea57bf7.jpg_r_240x160x90_02a57254.jpg',title:'斯文这下牛逼了',desc:'攻击力是现在的两倍'},
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

	.item
		overflow: hidden
		display flex
		height: 1.9rem

		.item-img
			width: 1.7rem
			height: 1.7rem
			padding: .1rem

		.item-info
			flex: 1
			min-width 0

			.item-title
				line-height .54rem
				font-size .32rem
				ellipsis()

			.item-desc
				line-height .4rem
				color: #ccc
				ellipsis()

			.item-button
				line-height .44rem
				margin-top .16rem
				color #fff
				background #ff9300
				border-radius .06rem
				padding 0 .2rem

</style>
