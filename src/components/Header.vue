<template>
  <header class="container">
    <div class="header-top">
      <div class="header-top-left">
        <h6>Download App <div class="ios">iOS</div>Advertise with us</h6>
      </div>
      <div class="header-top-right">
        <i class="fab fa-facebook-f"></i>
        <i class="fab fa-instagram"></i>
        <i class="fab fa-twitter"></i>
        <i class="fab fa-youtube"></i>
      </div>
    </div>
    <div class="header-between">
      <img class="center" src="../assets/img/avada-food-logo.png" alt="Logo Avada Food">
    </div>
    <div class="header-bottom">
      <div v-for="(link, index) in links" :key="index" class="headerLinks">
        <a :href="link.url">{{link.text}}</a>
      </div>
      <i class="fas fa-search"></i>
    </div>
    <!-- <i class="fas fa-search"></i> -->
  </header>
</template>

<script>
import Link from '../assets/data/Link.js';
export default {
  name: 'Header',
  data() {
    return{
      links: Link.headerLinks
    }
  }
}
</script>

<style scoped lang="scss">
@import "../style/generals";
.container{
  width: 100%;
  height: 170px;
  display: flex;
  flex-direction: column;
  align-items: center;

  .header-top{
    display: flex;
    width: 60%;
    height: 20px;
    justify-content: space-between;
    color: $color-cube-3;
    cursor: pointer;
    

    .ios{
      display: inline-block;
      text-align: center;
      vertical-align: middle;
      padding: 2px 6px;
      color: $mediam-cut-2;
      border-radius: 5px;
      background-color: $color-cube-5;
      margin-right: 10px;
    }
    i{
      margin-right: 20px;
    }
  }
  .header-between{
    height: 90px;

    img{
      height: 100%;
      display: inline-block;
      justify-content: center;
    }
  }
  
  .header-bottom{ 
    height: 50px; 
    width: 50%;
    margin-top: 25px;
    display: flex;
    justify-content: space-around;  

    a{        
      color: $color-cube-4;
      text-decoration: none;
    }
  }

  .fa-search{
    color: $color-cube-2;
  }
}
</style>
