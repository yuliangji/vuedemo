<template>
	<div class="content">
		<div class="inner">
			<div class="left">
				<slot></slot>
			</div><div class="right">
	      <transition name="fade" appear>
	      	<h1>
		        渐进式<br>JavaScript 框架
		      </h1>
	      </transition>
	      <p>
	        <a class="button" href="https://cn.vuejs.org/v2/guide/">起步</a>
	        <a class="button white" href="https://github.com/vuejs/vue" target="_blank">GITHUB</a>
	      </p>
	    </div>
		</div>
	</div>
</template>

<script type="text/ecmascript-6">
	export default{};
</script>

<style lang="stylus" rel="stylesheet/stylus">
	.content
		padding:50px 40px
		.inner
			width:900px
			margin:0 auto
			.left, .right
				display:inline-block
				vertical-align:top
			.left
				width:39%
				.logo-img
					width: 215px
					height: 215px
					float: right
					margin-right: 60px
			.right
				width:61%
				.fade-enter-active, .fade-leave-active {
				  transition: opacity 2s
				}
				.fade-enter, .fade-leave-active {
				  opacity: 0
				}
				h1
					margin:0
					font-size:3.2em
					font-weight:300
					color:#2c3e50
				p
					margin-top: 3em;
					a.button
						margin: 1em 0
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
						&:first-child
							margin-right:1em
					a.button.white
						background-color:#fff
						color:#4fc08d
</style>