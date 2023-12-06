
<template>
  <div class="hello">
    <p v-if="day == '1'">today monday</p>
    <p v-if="day == '2'">today tuesday</p>
    <p v-if="day == '3'"> today wensday</p>
    <p v-if="day == '4'">today thursday</p>
    <p v-if="day == '5'">today friday</p>
    <p v-if="day == '6'">today saturday</p>
    <p v-if="day == '0'">today sunday</p>
    
  </div>
</template>

<script>
  export default{
      data(){
        return{
          day:(new Date()).getDay(),
          
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