<script>
import {dcComics, shop, dc, sites, cta} from '../data/Footer-menus.js'

export default {
  name: 'myFooter',
  data(){
    return{
      dcComics,
      shop,
      dc,
      sites,
      cta,
    }
  }
}
</script>

<template>

  <div class="myFooterTop">

    <div class="container">
  
      <div class="col">
        <ul>
          <li
            v-for="(link, index) in dcComics"
            :key="index"><a href="#">{{link.text}}</a>
          </li>
        </ul>

        <ul>
          <li
            v-for="(link, index) in shop"
            :key="index"><a href="#">{{link.text}}</a>
          </li>
        </ul>
      </div>

      <div class="col">
        <ul>
          <li
            v-for="(link, index) in dc"
            :key="index"><a href="#">{{link.text}}</a>
          </li>
        </ul>
      </div>

      <div class="col">
        <ul>
          <li
            v-for="(link, index) in sites"
            :key="index"><a href="#">{{link.text}}</a>
          </li>
        </ul>
      </div>


      <div class="image">
        <img src="../assets/img/dc-logo-bg.png" alt="">
      </div>
  
    </div>

  </div>

  <div class="myFooterBottom">

    <div class="container">

      <div class="btn"><a href="#">SING-UP NOW!</a></div>

      <div class="cta">

        <span>FOLLOW US</span>

        <ul>
          <li v-for="(link, index) in cta"
            :key="index"><a href="#"><img :src="link.path"></a></li>
        </ul>

      </div>

    </div>

  </div>



</template>

<style lang="scss" scoped>

@use '../scss/partials/generals' as *;
@use '../scss/partials/vars' as *;
@use '../scss/partials/mixin' as *;

.myFooterTop{
  background-image: url('../assets/img/footer-bg.jpg');
  background-size: cover;
  overflow: hidden;

  .container{
    display: flex;
    height: 100%;

    .col{
      display: inline-block;
      width: 15%;
      padding: 3rem 0;

      li:first-child a{
        color: white;
        text-transform: uppercase;
        font-weight: bold;
        font-size: 1.2rem;
        margin-bottom: 1rem;
      }

      li a{
        color: $lightgray-color;
        margin-bottom: .3rem;
        font-size: .9rem;
        text-transform: capitalize;

        &:hover{
          color: white;
          cursor: pointer;
        }
      }

      li:last-child{
        margin-bottom: 1rem;
      }
    }

    .image{
      position: relative;

      img{
        position: absolute;
        left: 150px;
        scale: 1.5;
      }
    }
  }
}

.myFooterBottom{
  background-color: $darkgray-color;

  .container{
    @include centerFlex('between');
    padding: 2rem 0;
    .btn a{
      border: 2px solid $primary-color;
      color: white;
      padding: 10px 12px;

      &:hover{
        border: 2px solid white;
        color: $darkgray-color;
        background-color: $primary-color;
      }
    }

    .cta{
      @include centerFlex('vertical');

      span{
        color: $primary-color;
        font-weight: bold;
        margin-right: 1rem;
        font-size: 1.2rem;
      }
      li{
        display: inline-block;
        margin: 0 10px;

        &:hover img{
          scale: 1.2;
        }
      }
    }
  }
}

</style>