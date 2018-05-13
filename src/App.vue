<template>
	<!-- <div id='app' v-bind:class="{'acitved':isActived ,'error':isError }" :class="[acitveClass,errorClass,'wrn']" >
		{{message}}
		<input type="text" v-model="message"> -->

		<!-- <ul> -->
			<!-- 循环 1-->
			<!-- <li v-for="(item,index) in userData" v-bind:key='item'>
				{{index}}.{{item.name}},{{item.age}}
			</li> -->

			 <!-- 循环2 变量固定写法 (键 值 下标)-->
	<!-- 		<li v-for="(value, key ,index) in userData" v-bind:key="index">
				{{index+1}} {{key}} {{value}}
			</li>

		</ul>
		-->
		<!-- <p v-show="userData.gender === 'boy'">这是一个男</p>
		<p v-show="userData.gender === 'girl'">这是一个女</p>

		<input type="radio" name="sex"  value="a" v-model='radioC'>男
		<input type="radio" name="sex"  value="b" v-model='radioC'>女
		<p v-on:click="fnc">改变性别</p>
		{{firstName}}

		<p v-on:click="Fn">年龄+1</p>
		{{userData.age}} -->
	 <!-- 把导入的组件放到页面上 驼峰命名要改成小写 原来大写的前面加'-' -->
	<!-- 	<hellow></hellow>
 	</div> -->
 	<div id="app">
 		<add v-on:getAddData="getData"></add>
 		<list v-bind:listData="addList"></list>
 		<fnish></fnish>
 	</div>
</template>

<script>
//导入组件
// import hellow from '@/components/hellow.vue'
	// export default{
	// 	//注册导入的组件
	// 	components:{
	// 		hellow:hellow
	// 	},

	// 	name:'app',
	// 	data(){
	// 		return {
	// 			//循环 v-for 数组
	// 			// userData : [
	// 			// 	{
	// 			// 		name:'whj',
	// 			// 		age:'21',
	// 			// 	},
	// 			// 	{
	// 			// 		name:'dbb',
	// 			// 		age:'19'
	// 			// 	}
	// 			// ],
				
	// 			//v-for 对象
	// 			userData:{
					
	// 				name: 'zhangsan',
	// 				height: 170 ,
	// 				age: 21,
	// 				gender:'girl'
	// 			},

	// 			//性别
	// 			radioC: 'a',
	// 			//数组
	// 			acitveClass : 'active',
	// 			errorClass : 'error' ,
	// 			//对象
	// 			isError : true,
	// 			isActived : true,

	// 			className : 'App',
	// 			message:'hello world'
	// 		}
	// 	},
	// 	methods:{
	// 		fn: function (msg) {
	// 			// body...
	// 			alert(msg)
	// 		},
	// 		fnc (){
	// 			this.radioC='b';
	// 		},
	// 		Fn: function () {
	// 			this.userData.age++
	// 		}
	// 	},
	// 	computed:{

	// 		firstName(){
	// 			return this.message + 'whj';
	// 		}
	// 	},
	// 	watch:{
	// 		'userData.age':{
	// 			handler: function(val,oldval){
	// 				console.log('now:',val)
	// 				console.log('old:',oldval)
	// 			},
	// 			deep : true
	// 		}
	// 	}

	// }

import add from '@/components/add.vue'
import list from '@/components/list.vue'
import fnish from '@/components/fnish.vue'
	export default{
		// name:'app',
		components:{
			add,
			list,
			fnish
		},
		data (){
			return{
				addList:[]
			}
		},
		methods:{
			
			getData(val){
				// console.log(val)
				this.addList.push(val)
			}
		}
	}
</script>

<style scoped lang="scss">
@import "static/app";
@import url("../static/font-awesome-4.7.0/css/font-awesome.min.css")

</style>


