<template>
	<div class="highlights">
		<transition name="fade" appear>
			<div class="inner">
		    <div class="point">
		      <h2>易用</h2>
		      <p>已经会了HTML,CSS,JavaScript？即刻阅读指南开始构建应用！</p>
		    </div><div class="point">
		      <h2>灵活</h2>
		      <p>简单小巧的核心，渐进式技术栈，足以应付任何规模的应用。</p>
		    </div><div class="point">
		      <h2>性能</h2>
		      <p>
		        17kb min+gzip 运行大小<br>
		        超快虚拟 DOM <br>
		        最省心的优化
		      </p>
		    </div>
		  </div>
		</transition>
	</div>
</template>

<script type="text/ecmascript-6">
	export default{};
</script>

<style lang="stylus" rel="stylesheet/stylus">
	.highlights
		padding-bottom:70px
		.fade-enter-active, .fade-leave-active {
		  transition: opacity 2s
		}
		.fade-enter, .fade-leave-active {
		  opacity: 0
		}
		.inner
			width:900px
			margin: 0 auto
			text-align:center
			.point
				display:inline-block
				vertical-align:top
				width:33%
				box-sizing:border-box
				padding:0 2em
				h2
					color: #42b983
					font-size: 1.5em
					font-weight: 400
					margin: 0
					padding: 0.5em 0
				p
					margin:15px 0
					color: #7f8c8d
					word-spacing: 0.05em
					line-height:20px
</style>