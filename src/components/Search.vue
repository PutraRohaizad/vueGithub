<template>
<div class="m-5">
    <div class="bg-blue-900 p-5 text-center text-white">
        <h1><strong> Vue & Github API</strong></h1>
    </div>
    <div class="text-center">
         <form @submit.prevent="onSearch">
             <label class="text-black " for="search"><h1>Search for github user</h1></label>
        <input class="px-4 py-2 leading-tight" type="text" v-model="name" placeholder="Enter github name">
        <button class="m-2 p-2  bg-blue-300" v-on:click="getGithub">Search</button>

        </form>
    </div>
       
       
    <Result/>

</div>

</template>
<script>
import Result from "../components/Result"
import bus from '../bus'

export default {
    name : "Search",
    components:{
        Result
    },
    props: ["maklumats"],
    
    // Initiate Variable
    data() {
        return { name: '' }
    },
    methods:{
         onSearch() {
            if (this.name && this.name !== '') {
            bus.$emit('new-name', this.name)
            this.name = ''
      }
    }

    } 
}
</script>

<style scoped>

</style>