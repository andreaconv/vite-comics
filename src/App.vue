<script>

  import myHeader from './components/myHeader.vue'
  import myMain from './components/myMain.vue'
  import Brands from './components/Brands.vue'
  import myFooter from './components/myFooter.vue'

  export default {
  data(){
    return{

    }
  },
  components: {
    myHeader,
    myMain,
    Brands,
    myFooter,
  }
  }
</script>

<template>
  
  <myHeader />

  <myMain />

  <Brands />

  <myFooter />

</template>

<style lang="scss">

  @use './scss/main.scss';

</style>