<script>
import {headerMenu} from '../data/menus'

export default {
  name: 'myHeader',
  data(){
    return{
      headerMenu, 
    }
  }
}
</script>

<template>

  <div class="myHeader">

    <div class="container">
  
      <div class="image">
        <img src="../assets/img/dc-logo.png" alt="logo">
      </div>

      <ul>
        <li
          v-for="(item, index) in headerMenu"
          :key="index"
          :class="{'active' : item.isActive}">
          {{item.text}}
        </li>
      </ul>
  
    </div>
    
  </div>

</template>

<style lang="scss" scoped>

@use '../scss/partials/generals' as *;
@use '../scss/partials/vars' as *;
@use '../scss/partials/mixin' as *;

.myHeader{
  height: 100px;
}

.container{
  @include centerFlex('vertical');
  justify-content: space-between;
  height: 100%;
}

.image{
  height: 70%;
}

li{
  display: inline-block;
  text-transform: uppercase;
  margin-right: 2rem;
  color: $gray-color;
  font-weight: bold;
  font-size: .8rem;
  position: relative;
  cursor: pointer;

  &.active{
    color: $primary-color;

    &::after{
      position: absolute;
      bottom: -41px;
      left: 50%;
      content: "";
      background-color: $primary-color;
      width: 60%;
      height: 3px;
      transform: translate(-50%, 0);
    }
  }
}

</style>