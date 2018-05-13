<template>
	<div class="list">
		*****
		<ul>
			<li v-for="(item,index) in listData" v-bind:key="index">
				{{item}}
			</li>
		</ul>
	</div>
</template>
<style>
	
</style>
<script>
	export default{
		props:['listData'],

		data(){
			return{
				
			}
		},
	}
</script>