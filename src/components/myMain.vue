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

    <div class="jumbotron"></div>

    <div class="container">

      <div class="cards">carte</div>

    </div>

  </div>


</template>

<style lang="scss" scoped>

@use '../scss/partials/generals' as *;
@use '../scss/partials/vars' as *;


.myMain{
  background-color: $black-color;

  .jumbotron{
    height: 300px;
    background-image: url(../assets/img/jumbotron.jpg);
    background-size: cover;
  }

  .container{
    // debug
    height: 150px;
    color: white;
  }

}
  

</style>