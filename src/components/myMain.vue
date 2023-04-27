<script>
export default {
  name: 'myMain',
  data(){
    return{
      title: '-->Content goes here<--'
    }
  }
}
</script>

<template>

  <div class="myMain">

    <div class="container">

      <h2>{{title}}</h2>

    </div>


  </div>


</template>

<style lang="scss" scoped>

@use '../scss/partials/generals' as *;
@use '../scss/partials/vars' as *;


.myMain{
  height: 90px;
  background-color: $black-color;
}
  h2{
    color: white;
  }

</style>