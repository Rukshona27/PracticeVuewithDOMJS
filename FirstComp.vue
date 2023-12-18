<template>
   <div class="aa">
    <input type="checkbox" v-model="arr" value="v1" id="checkbox">
    <label for="checkbox">v1</label>
	<input type="checkbox" v-model="arr" value="v2" id="checkbox">
    <label for="checkbox">v2</label>
	<input type="checkbox" v-model="arr" value="v3" id="checkbox">
    <label for="checkbox">v3</label>
    <ul>
        <li v-for="el in arr">{{ el }}</li>
    </ul>
   </div>
</template>

<script>
    export default{
        data(){
            return{
                arr: [],
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