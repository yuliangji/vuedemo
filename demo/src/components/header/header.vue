<template>
	<div class="header">
		<a href="#" class="logo">
			Vue.js
		</a>
		<ul class="nav">
			<li>
				<input type="text" class="search">
			</li>
			
			<li v-for="item in navs">
				<a :href="item.href">{{item.title}}</a>
				<span v-if="item.children" class="arrow"></span>
				<ul v-if="item.children" class="nav-dropdown">
					<li v-for="dropdownItem in item.children">
						<a :href="dropdownItem.src"  target="_blank" class="nav-link" v-if="dropdownItem.title">
							{{dropdownItem.title}}
						</a>
						<h4 v-if="dropdownItem.h4">{{dropdownItem.h4}}</h4>
							<ul v-for="dropdownListItem in dropdownItem.children">
								<li><a :href="dropdownListItem.src" target="_blank">{{dropdownListItem.title}}</a></li>
							</ul>
					</li>
				</ul>
			</li>
		</ul>
	</div>
</template>

<script type="text/ecmascript-6">
	export default{
		data() {
			return {
				navs:data
			}
		}
	};
	var data= [{
		title: '教程',
		href: 'https://cn.vuejs.org/v2/guide/'
	},
	{
		title: 'API',
		href: 'https://cn.vuejs.org/v2/api/'
	},
	{
		title: '示例',
		href: 'https://cn.vuejs.org/v2/examples/'
	},
	{
		title: '参与贡献',
		href:'https://cn.vuejs.org/about/'
	},
	{
		title: '社区',
		children:[{
			title: 'GitHub',
			src:'https://github.com/vuejs/vue'
		},
		{
			title:'论坛',
			src: 'http://forum.vuejs.org'
		},
		{
			title:'聊天室',
			src:'https://gitter.im/vuejs/vue'
		},
		{
			title:'Twitter',
			src:'https://twitter.com/vuejs'
		},
		{
			title:'工作',
			src:'https://vuejsjob.com/?ref=vuejs'
		}]
	},
	{
		title: '生态系统',
		children:[{
			h4: '帮助',
			children:[{
				title: '论坛',
				src: 'http://forum.vuejs.org'
			},
			{
				title: '聊天室',
				src: 'https://gitter.im/vuejs/vue'
			},
			{
				title: '模板',
				src: 'https://github.com/vuejs-templates'
			}]
		},
		{
			h4:'信息',
			children:[{
				title: 'Twitter',
				src: 'https://twitter.com/vuejs'
			},
			{
				title: '博客',
				src: 'https://medium.com/the-vue-point'
			},
			{
				title: '工作',
				src: 'https://vuejobs.com/?ref=vuejs'
			}]
		},
		{
			h4:'核心插件',
			children:[{
				title: 'Vue Router',
				src: 'https://router.vuejs.org/'
			},
			{
				title: 'Vuex',
				src: 'https://vuex.vuejs.org/'
			}]
		},
		{
			h4:'资源列表',
			children:[{
				title: '官方仓库',
				src: 'https://github.com/vuejs'
			},
			{
				title: 'Vuex',
				src: 'https://github.com/vuejs/awesome-vue'
			}]
		}]
	},
	{
		title: '多语言',
		children:[{
			title: '中文',
			src:'https://cn.vuejs.org/'
		},
		{
			title:'English',
			src: 'https://vuejs.org/'
		},
		{
			title:'日本語',
			src:'https://jp.vuejs.org/'
		},
		{
			title:'Русский',
			src:'https://ru.vuejs.org/'
		},
		{
			title:'한국어',
			src:'https://kr.vuejs.org/'
		}]
	}];
</script>

<style lang="stylus" rel="stylesheet/stylus">
	.header
		background-color: #fff
		height: 60px
		padding: 10px 60px
		position: relative
		z-index: 2
		.logo
			display: inline-block
			font-size: 1.5em
			line-height: 40px
			color: #2c3e50
			font-family: 'Source Sans Pro', 'Helvetica Neue', Arial, sans-serif
			font-weight: 500
		.nav
			position:absolute
			right:60px
			top: 10px
			height:40px
			line-height:40px
			font-size:0
			li
				display:inline-block
				position:relative
				margin:0 0.6em
				font-size:15px
				&:hover .nav-dropdown
					display:block
				.search
					height: 30px;
					line-height: 30px;
					box-sizing: border-box;
					padding: 0 15px 0 30px;
					border: 1px solid #e3e3e3;
					color: #2c3e50;
					outline: none;
					border-radius: 15px;
					margin-right: 10px;
					transition: border-color 0.2s ease;
					background: #fff url('https://cn.vuejs.org/images/search.png') 8px 5px no-repeat;
					background-size: 20px;
					vertical-align: middle !important;
					&:focus
						border-color: #42b983;
				.arrow
					display: inline-block;
					vertical-align: middle;
					margin-top: -1px;
					margin-right: -14px;
					width: 0;
					height: 0;
					border-left: 4px solid transparent;
					border-right: 4px solid transparent;
					border-top: 5px solid #ccc;
				.nav-dropdown
					display:none
					box-sizing: border-box;
					max-height: calc(100vh - 61px);
					overflow-y: scroll;
					position: absolute;
					top: 100%;
					right: -15px;
					background-color: #fff;
					padding: 10px 0;
					border: 1px solid #ddd;
					border-bottom-color: #ccc;
					text-align: left;
					border-radius: 4px;
					white-space: nowrap;
					li
						display:block
						line-height:1.8em
						margin:0
						a
							font-size:0.9em
							display:block
							padding: 0 24px 0 20px;
							&:hover
								color:#42b983
						h4
							padding: 0 24px 0 20px;
							font-weight: 600
</style>