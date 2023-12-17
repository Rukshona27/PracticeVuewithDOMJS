
<script>
import first from './components/firstComponent.vue';
  export default {
    data() {
	  return {
      arr:[
        {id:1, name:'dog', age: 7, quantity: 2},
        {id:2, name:'rabbit', age: 4, quantity: 4},
        {id:3, name:'cat', age: 6, quantity: 1},
      ]
	}
},methods:{
  remove(id){
    this.arr = this.arr.filter((arr0)=>{
      return arr0.id !== id
    });
  }
},
components: { first}
}
</script>

<template>
  <first v-for="arr0 in arr"
    :id="arr0.id"
    :name="arr0.name"
    :quantity="arr0.quantity"
    :age="arr0.age"
    :key="arr0.id"
    @remove="remove"/>
</template>

<style scoped>

</style>
