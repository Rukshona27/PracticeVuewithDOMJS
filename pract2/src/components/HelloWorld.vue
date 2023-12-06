
<template>
  <div>
    <p v-if="age<18">подросток</p>
    <p v-else-if="age==19 || age<=25">молодой человек</p>
    <p v-else-if="age>=26">мужчина</p>
    <p v-else>error</p>
  </div>
</template>

<script>
  export default{
      data(){
        return{
          age:15,
        };
      },
      methods:{
        
      }
  };
</script>
<style scoped>
.hello{
  font-size: 6em;
}
</style>