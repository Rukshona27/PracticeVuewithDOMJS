

<template>
	<div class="aa">
		<input v-model="num">
	<input  v-model="num2">
	<input  v-model="num3">
	<p>{{ res}}</p>
	<button @click="resBtn">btn</button>
	</div>
</template>


<script>
  export default{
    data() {
	return{
		num:0,
		num2:0,
		num3:0,
		arr:[],
	}
	},
	methods:{
		resBtn:function(){
			let i = 0;
			this.arr = (this.num).split('-')
			while (i<this.arr.length) {
				this.num = this.arr[i];
				i++;
				this.num2 = this.arr[i];
				i++;
				this.num3 = this.arr[i];
				i++;
			}
		}
	}
}
</script>
<style>
	.aa{
		font-size: 2em;
	}
</style>

