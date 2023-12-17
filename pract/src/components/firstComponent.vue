<template>
    <div class="aa">
        <template v-if="!isEdit">
            {{ name }} {{ age }} {{ quantity }}
            <button @click="edit">edit</button>
        </template>
        <template v-else>
            <input v-model="newName" type="text">
            <input v-model="newAge" type="text">
            <input v-model="newQuantity" type="text">
            <button @click="save">save</button>
        </template>
    </div>
</template>

<script>
    export default{
        props:['id', 'name', 'age', 'quantity'],
        data(){
            return{
                isEdit:false,
                newName: this.name,
                newAge:this.age,
                newQuantity:this.quantity
            }
        },
        emits:['change'],
        methods:{
            edit:function(){
                this.isEdit = true;
            },
            save:function(){
                this.isEdit = false;
                this.$emit('change', this.id, this.name, this.age, this.quantity) 
            }
        }
    }
</script>


<style>
.aa{
    font-size: 1em;
}
</style>