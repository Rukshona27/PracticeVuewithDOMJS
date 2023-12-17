
<script>
import first from './components/firstComponent.vue';
  export default {
    data() {
	  return {
      arr1:[
        {id:1, name:'dog', age: 7, quantity: 2},
        {id:2, name:'rabbit', age: 4, quantity: 4},
        {id:3, name:'cat', age: 6, quantity: 1},
      ]
	}
},methods:{
    change(id, name, age, quantity){
      this.arr1 = this.arr1.map((arr)=>{
        if(arr.id === id){
          arr.name = name;
          arr.age = age;
          arr.quantity = quantity;
        };
        return arr;
      })
    }
},
components: { first}
}
</script>

<template>
  <first v-for="arr in arr1"
    :id="arr.id"
    :name="arr.name"
    :quantity="arr.quantity"
    :age="arr.age"
    :key="arr.id"
    @change="change"
    />
</template>

<style scoped>

</style>
