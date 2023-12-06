<template>
  <table>
    <template v-for="prod in products">
      <tr class="div">
        <td>{{ prod.name }}</td>
        <td>-</td>
        <td>{{ prod.price }}</td>
        <td>-</td>
        <td>{{ prod.quantity }}</td>
      </tr>
    </template>
  </table>
</template>

<script>
  export default{
    data() {
	  return {
		products: [
			{
				name: 'product1',
				price: 100,
				quantity: 5
			},
			{
				name: 'product2',
				price: 200,
				quantity: 4
			},
			{
				name: 'product3',
				price: 300,
				quantity: 3
			},
		]
	}
}
,
    methods:{

    }
  };
</script>
<style scoped>
.div{
  font-size: 5em;
}
</style>