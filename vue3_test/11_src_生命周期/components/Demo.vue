<template>
	<h2>当前求和为：{{sum}}</h2>
	<button @click="sum++">点我+1</button>
	<hr>
	<h2>当前点击时鼠标的坐标为：x：{{point.x}},y: {{point.y}}</h2>
</template>

<script>
	import {ref,reactive,onMounted,onBeforeUnmount} from 'vue'
	export default {
		name: 'Demo',
		setup(){
			//数据
			let sum = ref(0)
			let point = reactive({
				x:0,
				y:0
			})

			//方法
			function savePoint(event){
				
			}

			onMounted(()=>{
				window.addEventListener('click',savePoint)
			})

			onBeforeUnmount(()=>{
				window.removeEventListener('click',savePoint)
			})

			//返回一个对象（常用）
			return {sum,point}
		}
	}
</script>