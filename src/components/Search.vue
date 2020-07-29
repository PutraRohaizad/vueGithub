<template>
<div class="m-5">
    <div class="bg-blue-900 p-5 text-center text-white">
    <h1><strong> PUTRAHUB</strong></h1>
    </div>
    <div class="text-center " v-bind:key="maklumat.id" v-for="maklumat in maklumats">
        <label class="text-black " for="search"><h1>Search for github user</h1></label>
        <input class="px-4 py-2 leading-tight" type="text" name="search" placeholder="github name">
        <button class="m-2 p-2  bg-blue-300" v-on:click="getGithub">Search</button>
    </div>

    <Result/>


</div>

</template>
<script>
import Result from "../components/Result"

export default {
    name : "Search",
    components:{
        Result
    },
    props: ["maklumats"],
    methods:{
         getGithub() {
            fetch('https://api.github.com/')
            .then(res => res.json())
            .then(data => console.log(data))
         }
    } 
}
</script>

<style scoped>

</style>