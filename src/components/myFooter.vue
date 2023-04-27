<script>
import {dcComics, shop, dc, sites} from '../data/Footer-menus.js'

export default {
  name: 'myFooter',
  data(){
    return{
      dcComics,
      shop,
      dc,
      sites,
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
            :key="index">
            {{link.text}}
          </li>
        </ul>

        <ul>
          <li
            v-for="(link, index) in shop"
            :key="index">
            {{link.text}}
          </li>
        </ul>
      </div>

      <div class="col">
        <ul>
          <li
            v-for="(link, index) in dc"
            :key="index">
            {{link.text}}
          </li>
        </ul>
      </div>

      <div class="col">
        <ul>
          <li
            v-for="(link, index) in sites"
            :key="index">
            {{link.text}}
          </li>
        </ul>
      </div>

      <!-- TODO: [ADD] image -->

      <div class="image">
        <img src="../assets/img/dc-logo-bg.png" alt="">
      </div>
  
    </div>

  </div>

  <div class="myFooterBottom">

    <div class="container">

      

    </div>

  </div>



</template>

<style lang="scss" scoped>

@use '../scss/partials/generals' as *;
@use '../scss/partials/vars' as *;

.myFooterTop{
  height: 400px;
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

      li:first-child{
        color: white;
        text-transform: uppercase;
        font-weight: bold;
        font-size: 1.2rem;
        margin-bottom: 1rem;
      }

      li{
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
  height: 100px;
  background-color: $darkgray-color;
}

</style>