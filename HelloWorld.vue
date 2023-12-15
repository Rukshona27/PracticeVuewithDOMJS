<template>
 <p>{{ name }}</p>
 <p>  {{ salary }}</p> 
 <p>  {{ age }} </p>
</template>

<script>
  export default{
    props:{
      name: String,
      age:Number,
      salary:Number,
      id: Number
    },
    data(){
      return {
      }
    }
  }

</script>


<style scoped>

</style>
