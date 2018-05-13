<template>
	<div class="add">
		<p>请输入</p>
		<input type="text" name="" v-model="inputValue">
		{{inputValue}}
		<p>
			<button v-on:click="addTodo">确定添加</button>
		</p>

	</div>
</template>
<style>
	
</style>
<script>
	export default{
		data (){
			return{
				inputValue:''
			}
		},
		methods:{
			addTodo(){
				this.$emit('getAddData',this.inputValue)
			}
		}
	}
</script>