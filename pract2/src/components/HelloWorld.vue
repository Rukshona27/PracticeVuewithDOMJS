
<template>
  <div class="hello">
    <button @click="counter+=1">+1</button>
    <p>button click {{ counter }}</p>
  </div>
</template>


<script>
  export default{
      data(){
        return{
         counter: 0,
        };
      },
  };
</script>
<style scoped>
.hello{
  font-size: 3em;
}
</style>