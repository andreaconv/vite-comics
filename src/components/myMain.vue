<script>
import Cards from './partials/cards.vue';
import Comics from '../data/dc-comics.json';

export default {
  name: 'myMain',
  components: {
    Cards
  },
  data(){
    return{
      Comics,
    }
  }
}
</script>

<template>

  <div class="myMain">

    <div class="jumbotron"></div>

    <div class="container">

      <span id="abs">CURRENT SERIES</span>

      <div class="main-wrapper">

        <Cards :elenco="Comics"/>

      </div>
      
      <div class="btn">LOAD MORE</div>

    </div>

  </div>


</template>

<style lang="scss" scoped>

@use '../scss/partials/generals' as *;
@use '../scss/partials/vars' as *;
@use '../scss/partials/mixin' as *;


.myMain{
  background-color: $black-color;

  .jumbotron{
    height: 300px;
    background-image: url(../assets/img/jumbotron.jpg);
    background-size: cover;
  }

  .container{
    position: relative;
    padding: 20px 0;
    color: white;

    .main-wrapper{
      @include centerFlex('wrap-ween');
      margin-bottom: 1rem;
    }

    .btn{
      text-align: center;
      max-width: 150px;
      margin: 0 auto;
      padding: 10px;
      background-color: $primary-color;

      &:hover{
        cursor: pointer;
        scale: 1.1;
      }
    }

    span#abs{
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