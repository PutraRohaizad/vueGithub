<template>
<div>
    <div class="container text-red-300">
        <div class="text-red-300" v-bind:key="maklumat.id" v-for="maklumat in maklumats">
            <h1>{{maklumat.name}}</h1>
        </div>
    </div>
    
</div>

</template>

<script>
export default {
    name : "Search",
    props: ["maklumats"]
}
</script>

<style scoped>

</style>