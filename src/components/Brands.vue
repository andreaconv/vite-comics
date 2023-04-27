<script>
import {brands} from '../data/Brands-menu.js'

export default {
  name: 'Brands',
  data(){
    return{
      brands,
    }
  }
}
</script>

<template>

  <div class="brands">

    <div class="container">
  
      <ul>
        <li
            v-for="(link, index) in brands"
            :key="index">
          <img :src="link.path">
          <a href="#">{{link.text}}</a>
        </li>
      </ul>
  
    </div>

  </div>



</template>

<style lang="scss" scoped>

@use '../scss/partials/generals' as *;
@use '../scss/partials/vars' as *;
@use '../scss/partials/mixin' as *;


.brands{
  height: 120px;
  background-color: $primary-color;

  .container{
    @include centerFlex('vertical');
    height: 100%;

    ul{
      display: flex;
      justify-content: space-evenly;
      width: 100%;
    }

    li{
      @include centerFlex('vertical');

      &:hover a{
        color: $lightgray-color;
      }

      // FIXME: all'hover vorrei che l'immagine diventi grigia
      &:hover img{
        filter: grayscale(1);
      }

      img{
        height: 40px;
        margin-right: 1rem;
      }

      a{
        color: white;
        text-transform: uppercase;
      }

      &:last-child img{
          height: 30px;
        }
    }
  }
}

</style>