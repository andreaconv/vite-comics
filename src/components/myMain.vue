<script>
import Comics from '../data/dc-comics.json';

export default {
  name: 'myMain',
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
        <div
          class="card"
          v-for="(comic, index) in Comics"
          :key="index">
          <img :src="comic.thumb">
          <span>{{comic.series}}</span>
        </div>
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
      // width: 100%;
      margin-bottom: 1rem;

      .card{
        width: calc(100% / 6 - 20px);
        margin: 1.5rem 0;

        img{
          width: 100%;
          aspect-ratio: 2 / 3;
          margin-bottom: 1rem;

          &:hover{
            scale: 1.1;
          }
        }

        span{
          text-transform: uppercase;
        }
      }
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
      left: -15px;
      top: 0;
      transform: translate(0, -50%);
    }
  }

}
  

</style>