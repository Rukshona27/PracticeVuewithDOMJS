<template>
    <div class="aa">
       {{ id }} {{ name }} {{ age }} {{ quantity }}

        <button v-on:click="$emit('remove', id)">remove</button>
    </div>
</template>

<script>
    export default{
        props:['id', 'name', 'age', 'quantity'],
        emits:['remove'],
    }
</script>
<style>
.aa{
    font-size: 1em;
}
</style>