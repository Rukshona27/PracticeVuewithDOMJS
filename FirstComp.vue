<template>
   <div class="aa">
    <input type="radio" value="v1" v-model="choice" >
    <input type="radio" value="v2" v-model="choice" >
    <input type="radio" value="v3" v-model="choice" >
    <input type="radio" value="v4" v-model="choice" >
    <p>you choiced: {{ choice }}</p>
    <p>Only one to choose from</p>
   </div>
</template>

<script>
    export default{
        data(){
            return{
                choice:''
            }
        }
    }
</script>

<style>
.aa{
    font-size: 2em;
};
hr{
    color:blueviolet
}
</style>