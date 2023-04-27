<script>
export default {
  name: 'myFooter',
  data(){
    return{
      title: 'myFooter'
    }
  }
}
</script>

<template>

  <div class="myFooterTop">

    <div class="container">
  
      <div class="col">
        <ul>
          <li>dc comics</li>
          <li>characters</li>
          <li>comics</li>
          <li>movies</li>
          <li>tv</li>
          <li>games</li>
          <li>Videos</li>
          <li>news</li>
        </ul>

        <ul>
          <li>shop</li>
          <li>shop DC</li>
          <li>shop DC collectibles</li>
        </ul>
      </div>

      <div class="col">
        <ul>
          <li>DC</li>
          <li>Terms of us</li>
          <li>privacy policy (new)</li>
          <li>privacy policy (new)</li>
          <li>privacy policy (new)</li>
          <li>privacy policy (new)</li>
          <li>privacy policy (new)</li>
          <li>privacy policy (new)</li>
          <li>privacy policy (new)</li>
          <li>privacy policy (new)</li>
          <li>privacy policy (new)</li>
          <li>privacy policy (new)</li>
        </ul>
      </div>

      <div class="col">
        <ul>
          <li>sites</li>
          <li>dc</li>
          <li>mad magazine</li>
          <li>mad magazine</li>
          <li>mad magazine</li>
          <li>mad magazine</li>
        </ul>
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
  }
}

.myFooterBottom{
  height: 100px;
  background-color: $darkgray-color;
}

</style>