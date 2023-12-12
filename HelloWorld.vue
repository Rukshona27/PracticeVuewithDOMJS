<template>
	<div>
	  <p>Цена за литр топлива: {{ fuel.pricePerLiter }}</p>
	  <p>Количество литров: {{ fuel.liters }}</p>
	  <p>Итоговая стоимость: {{totalCost}}</p>
	  <button @click="changeLiters">Изменить количество топлива</button>
	</div>
  </template>
  
  
  
  <script>
  export default{
  data(){
	return{
	  fuel: {
		pricePerLiter: 50,
		liters: 15,
	   }
	  };
	},
	computed: {
	  totalCost() {
		return this.fuel.pricePerLiter*this.fuel.liters;
	  }
	},
	methods: {
	  changeLiters() {
		let newLiters = prompt('Введите новое количество топлива:');
		if (newLiters !==null || !isNaN(newLiters)){
		  this.fuel.liters = parseFloat(newLiters);
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

