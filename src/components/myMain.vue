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

      <span id="abs">CURRENT SERIES</span>

      <div class="main-wrapper">
        <div class="card">
          <img src="https://www.coverbrowser.com/image/action-comics/1-1.jpg" alt="">
          <span>testo</span>
        </div>
        <div class="card">
          <img src="https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg" alt="">
          <span>American Vampire 1976</span>
        </div>
        <div class="card">
          <img src="https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg" alt="">
        </div>
        <div class="card">
          <img src="https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg" alt="">
        </div>
        <div class="card">
          <img src="https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg" alt="">
        </div>
        <div class="card">
          <img src="https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg" alt="">
        </div>
        <div class="card">
          <img src="https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg" alt="">
        </div>
        <div class="card">
          <img src="https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg" alt="">
          <span>Batman: White Knight Presents: Harley Quinn</span>
        </div>
        <div class="card">
          <img src="https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg" alt="">
          <span>Batman: White Knight Presents: Harley Quinn</span>
        </div>
        <div class="card">
          <img src="https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg" alt="">
          <span>Batman: White Knight Presents: Harley Quinn</span>
        </div>
        <div class="card">
          <img src="https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg" alt="">
          <span>Batman: White Knight Presents: Harley Quinn</span>
        </div>
        <div class="card">
          <img src="https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg" alt="">
          <span>Batman: White Knight Presents: Harley Quinn</span>
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
          aspect-ratio: 1 / 1;
          margin-bottom: 1rem;
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