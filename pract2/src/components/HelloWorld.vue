
<template>
  <div class="hello">
    <p v-if="!visibleTrue">text true</p>
    <p v-if="visibleFalse">text false</p>
  </div>
</template>

<script>
  export default{
      data(){
        return{
          visibleTrue: true,
          visibleFalse: true,
        };
      },
      methods:{
      }
  };
</script>
<style scoped>
.hello{
  font-size: 3em;
}
</style>