<template>
  <div class="text-center">
      <table class="table-auto">
          <thead>
              <tr>
                  <th>#</th>
                  <th>Name</th>
                  <th>URL</th>
              </tr>
          </thead>
          <tbody>
              <tr>
                  <td>1</td>
                  <td>test</td>
                  <td>testets</td>
              </tr>
          </tbody>
      </table>
  </div>
</template>

<script>
export default {
    name:"Result",
    method:[{
         getGithub() {
         console.log('3232');   
        }
    }],
}
</script>

<style>

</style>