<template>
	<div id="app">
		<span>{{ title }}</span>
	</div>
</template>

<script>
import HelloWorld from './components/HelloWorld'

export default {
	name: 'app',
	data () {
		return {
			title:'Vue.js Demo'
		}
	}/*,
	beforeCreated:function(){
		console.log("beforeCreated： 组件被实例化之前！");
	},
	created: function(){
		console.log("组件实例化完毕，但页面还未显示");
	},
	beforeMount:function(){
		console.log("组件挂载前，页面仍然未展示，页面显示");
	},
	mounted:function(){
		console.log("组件挂载后，此方法执行后，页面展示");
	},
	beforeUpdate:function(){
		console.log("组件更新前，页面仍未更新，但是虚拟DOM已经配置");
	},
	updated:function(){
		console.log("组件更新后，此方法执行后，页面显示");
	},
	beforeDestrory:function(){
		console.log("组件销毁前");
	},
	destroryed: function(){
		console.log("组件销毁后");
	}*/
}

</script>


