<script>
export default {
  name: 'myHeader',
  data(){
    return{
      title: 'myHeader'
    }
  }
}
</script>

<template>

  <div class="myHeader">

    <div class="container">
  
      <h1>{{title}}</h1>
  
    </div>
    
  </div>

</template>

<style lang="scss" scoped>

@use '../scss/partials/generals' as *;
@use '../scss/partials/vars' as *;

.myHeader{
  height: 80px;
  background-color: $primary-color;
}


</style>