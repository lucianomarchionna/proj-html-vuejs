<template>
  <header class="container">
    <div class="header-top">
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
  height: 150px;
  display: flex;
  flex-direction: column;
  align-items: center;

  .header-top{
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
