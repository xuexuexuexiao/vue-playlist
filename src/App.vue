<template>
  <div id="app">
    <ul>
      <li><router-link to="/">Home</router-link></li>
      <li><router-link to="/helloworld">HelloWorld</router-link></li>
    </ul>
  </div>
</template>

<script >
  
  export default {
     name:'app',
     data(){
      return{

      }
     }
  }
</script>

<style scoped>
 h1{
  color:purple;
 }

</style>