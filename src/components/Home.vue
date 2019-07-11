<!-- 1模板：html结构 -->
<template>
	<div id="home">
		<app-header v-on:titleChange="updateTitle($event)" v-bind:title="title"></app-header>
		<users v-bind:users="users"></users>
		<app-footer v-bind:title="title"></app-footer>
	</div>
</template>

<!-- 2行为：处理逻辑 -->
<script >
	//注册局部组件
import Users from './Users'
import Header from './Header'
import Footer from './Footer'

export default {
	name: 'home',
	data () {
		return {
			users:[],
			title:'传递的是一个值，（number string boolean）'
		}
	},
	methods:{
		updateTitle(title){
			this.title = title;
		}
	},
	components:{
		"users":Users,
		"app-footer":Footer,
		"app-header":Header
	},
	created(){
		this.$http.get("http://jsonplaceholder.typicode.com/users").then((data) => {
			console.log(data);
			this.users = data.body;
		})
	}
}
</script>

<!-- 3样式：解决样式 -->
<style scoped>
	h1{
		color:purple;
	}
</style>

