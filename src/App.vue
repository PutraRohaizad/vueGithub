<template>
  <div id="app">
    <Search v-bind:maklumats="details"/>
  </div>
</template>
<script>
import Search from './components/Search'
import './assets/styles/app.css';

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
