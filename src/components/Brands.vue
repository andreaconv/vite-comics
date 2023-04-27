<script>
export default {
  name: 'Brands',
  data(){
    return{
      title: 'Brands'
    }
  }
}
</script>

<template>

  <div class="brands">

    <div class="container">
  
      <h1>{{title}}</h1>
  
    </div>

  </div>



</template>

<style lang="scss" scoped>

@use '../scss/partials/generals' as *;
@use '../scss/partials/vars' as *;

.brands{
  height: 120px;
  background-color: $primary-color;
}
  h1{
    color: white;
  }

</style>