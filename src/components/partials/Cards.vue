  <script>
  export default {
    name: 'Cards',
    props: {
      elenco: Array, // Object, Array, String, Integer, Boolean
    }
  }
  </script>

  
<template>
  
  <div
    class="card"
    v-for="(comic, index) in elenco"
    :key="index">
    <img :src="comic.thumb">
    <span>{{comic.series}}</span>
  </div>

</template>

<style lang="scss" scoped>

.card{
  width: calc(100% / 6);
  margin: 1.5rem 0;
  padding: 0 10px;

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

</style>