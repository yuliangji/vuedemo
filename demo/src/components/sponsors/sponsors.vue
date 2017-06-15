<template>
	<div class="sponsors">
	  <transition name="fade" appear>
	  	<div class="inner">
		    <h3>赞助者</h3>
		    <a href="https://www.upyun.com/?utm_source=vue&amp;utm_medium=ad&amp;utm_content=index" target="_blank" style="width:160px">
				  <img src="https://cn.vuejs.org/images/upyun-large.png" style="width:160px">
				</a>
				<br>
				<a  v-for="item in links" :href="item.href" :style="item.linkStyle">
					<img :src="item.imgSrc" :style="item.style">
				</a>
		    <br>
		    <a class="become-sponsor" href="https://cn.vuejs.org/support-vuejs/">成为赞助者</a>
		  </div>
	  </transition>
</div>
</template>

<script type="text/ecmascript-6">
	export default{
		data() {
			return {
				links: data
			}
		}
	};
	var data = [
	{
		href:'https://stdlib.com/',
		imgSrc:'https://cn.vuejs.org/images/stdlib.png',
	},
	{
		href:'https://deepstreamhub.com',
		imgSrc:'https://cn.vuejs.org/images/deepstream.png',
		linkStyle:'width:130px;top:1px',
		style: 'width:130px'
	},
	{
		href:'https://jsfiddle.net/',
		imgSrc:'https://cn.vuejs.org/images/jsfiddle.png',
	},
	{
		href:'https://laravel.com/',
		imgSrc:'https://cn.vuejs.org/images/laravel.png',
	},
	{
		href:'https://chaitin.cn',
		imgSrc:'https://cn.vuejs.org/images/chaitin.png',
	},
	{
		href:'https://htmlburger.com',
		imgSrc:'https://cn.vuejs.org/images/htmlburger.png',
	},
	{
		href:'https://starter.someline.com/',
		imgSrc:'https://cn.vuejs.org/images/someline.png',
		linkStyle:'top:-2px'
	},
	{
		href:'http://monterail.com/',
		imgSrc:'https://cn.vuejs.org/images/monterail.png',
	},
	{
		href:'https://www.trisoft.ro/',
		imgSrc:'https://cn.vuejs.org/images/trisoft.png',
		linkStyle:'top:-2px',
		style:'width:80px'
	},
	{
		href:'https://www.2mhost.com/',
		imgSrc:'https://cn.vuejs.org/images/2mhost.png',
		linkStyle:'width:90px',
		style:'width:90px'
	},
	{
		href:'https://vuejobs.com/?ref=vuejs',
		imgSrc:'https://cn.vuejs.org/images/vuejobs.svg',
		linkStyle:'width:80px;top:4px',
		style:'width:80px'
	},
	{
		href:'https://leanpub.com/vuejs2',
		imgSrc:'https://cn.vuejs.org/images/tmvuejs2.png',
	},
	{
		href:'https://famebroker.com',
		imgSrc:'https://cn.vuejs.org/images/famebroker.png',
		linkStyle:'width:115px',
		style:'width:115px'
	},
	{
		href:'https://fancygrid.com',
		imgSrc:'https://cn.vuejs.org/images/fancygrid.png',
		linkStyle:'width:110px;',
		style:'width:110px;'
	},
	{
		href:'https://component.io',
		imgSrc:'https://cn.vuejs.org/images/component_io.png',
		linkStyle:'width:120px;top:1px',
		style:'width:120px'
	},]
</script>

<style lang="stylus" rel="stylesheet/stylus">
	.sponsors
		padding: 35px 40px 45px
		text-align: center
		background-color: #f6f6f6
		.fade-enter-active, .fade-leave-active {
		  transition: opacity 2s
		}
		.fade-enter, .fade-leave-active {
		  opacity: 0
		}
		.inner
			width:700px
			margin:0 auto
			h3
				margin: 0 0 10px
				font-size:0.9em
				color:#999
			a, img
				width:100px
				display:inline-block
				vertical-align:middle
			a
				position:relative
				margin:20px 15px 0
			img
				transition: all 0.3s ease
				filter: grayscale(100%)
				opacity: 0.66
			a.become-sponsor
				padding: 0.75em 2em
				border-radius: 2em
				display: inline-block
				color: #fff
				background-color: #4fc08d
				transition: all 0.15s ease
				box-sizing: border-box
				border: 1px solid #4fc08d
				font-size: 1.05em
				font-weight: 600
				letter-spacing: 0.1em
				margin-top: 40px
				font-size: 0.9em
				font-weight: 700
				width: auto
				background-color: transparent
				color:#4fc08d
</style>