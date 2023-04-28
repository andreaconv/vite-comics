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

      <span>CURRENT SERIES</span>

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
    position: relative;
    // debug
    height: 150px;
    // altezza da modificare col contenuto e col padding
    color: white;

    span{
      padding: 10px 20px;
      font-weight: bold;
      background-color: $primary-color;
      position: absolute;
      left: 0;
      top: 0;
      transform: translate(0, -50%);
    }
  }

}
  

</style>