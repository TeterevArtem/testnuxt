<template>
  <div class="container header__container">
    <div class="header d-flex justify-content-between">
      <div class="header__block haeader__block_left col-0 col-lg-2" >     
        <div class="logo">
          <img class="logo__img" src="~/assets/images/logo.png" alt="logo">
        </div>      
      </div>
      <div class="header__block haeader__block_right col-md-10 col-12">
        <h2 class="header__title">My account</h2>
        <Navbar/>
      </div>
    </div>
  </div>
</template>

<script>

import Navbar from '~/components/Navbar'

export default {
  components: {
    Navbar
  }
}

</script>

<style lang="scss">
  // .header__container{
  //   padding: 0
  // }
  .logo{
    width: 98px;
    height: 98px;
    box-shadow: 0 2px 3px rgba(0,0,0,.3);
    overflow: hidden;
    @media screen and(max-width: 767px){
      display: none
    }
  }
  .logo__img{
    width: 100%;
    height: auto;
  }
  .header__title{
    margin-bottom: 5px;
    margin-left: 25px;
    color: red;
  }
  .header__block{
    padding: 0
  }
</style>