
<template>
  <div class="hello">
    <button v-on:click="toggle">toggle</button>
    <p v-if="visible">text</p>
  </div>
</template>

<script>
  export default{
      data(){
        return{
          visible:true,
        };
      },
      methods:{
        toggle:function(){
            this.visible = !this.visible;
        }
      }
  };
</script>
<style scoped>
.hello{
  font-size: 3em;
}
</style>