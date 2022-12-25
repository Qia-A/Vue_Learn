<template>
	<div>
		<School></School>
		<Stundent></Stundent>
	</div>
</template>

<script>
	//引入组件
	import School from './School.vue'
	import Stundent from './Student.vue'

	export default {
		name:'App',
		components:{
			School,
			Stundent
		}
	}
</script>

<style>

</style>