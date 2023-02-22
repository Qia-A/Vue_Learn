<template>
	<div>
		<img src="./assets/logo.png" alt="">
		<School></School>
		<Stundent></Stundent>
	</div>
</template>

<script>
	//引入组件
	import School from './components/School'
	import Stundent from './components/Student'

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