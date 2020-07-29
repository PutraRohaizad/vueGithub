<template>
  <div id="app">
    <Search class="bg-gray-300" v-bind:maklumats="details"/>
  </div>
</template>
<script>
import Search from './components/Search'
import './assets/styles/index.css';

export default {
  name: 'App',
  components: {
    Search
  },

  data(){
    return {
      details:[{
      id: 1,
      name: "Putra",
      age:24
      }
      ]
    }
  }
}
</script>

<style>

</style>
