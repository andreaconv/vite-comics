<script>
export default {
  name: 'myFooter',
  data(){
    return{
      title: 'myFooter'
    }
  }
}
</script>

<template>

  <div class="myFooter">

    <div class="container">
  
      <h1>{{title}}</h1>
  
    </div>

  </div>



</template>

<style lang="scss" scoped>

@use '../scss/partials/generals' as *;
@use '../scss/partials/vars' as *;

.myFooter{
  height: 500px;
  background-color: $darkgray-color;
}
  h1{
    color: white;
  }

</style>