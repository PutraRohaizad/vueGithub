<template>
  <div class="text-center">
    <div class="flex mb-4">
        <div class="w-1/3"></div>
        <div class="w-1/3 text-red-500">Profile</div>
        <div class="w-1/3 text-left">
            <h2 class="text-red-500">Details</h2> 
            <div>
                Name : Putra
            </div>
            <div>
                Name : Putra
            </div>
            <div>
                Repositories : 10
            </div>
            <div>
                Website : Putra
            </div>
        </div>
    </div>

  </div>
</template>

<script>
import bus from '../bus'
import Vue from 'vue'

export default {
  name: "Result",

 // Initiate variable
   data() {
    return {
      currentName: null,
      githubData: {}
    }
  },

// Life cycle
  created() {
    bus.$on('new-name', this.onNameChange)
  },
  destroyed() {
    bus.$off('new-name', this.onNameChange)
  },

// Function
  method: {
       onNameChange(name) {
            this.currentName = name
            this.fetchGithubData(name)
        },
         getGithub() {
            fetch('https://api.github.com/users/putrarohaizad')
            .then(res => res.json())
            .then(data => {
                console.log(data);
                Vue.set(this.githubData, name, data)

            })
         }
  }
};
</script>

<style></style>
