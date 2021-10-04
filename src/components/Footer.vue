<template>
  <footer class="container-small">
    <div class="top-footer">
      <div class="left-footer">
        <img src="../assets/img/avada-food-logo-footer.png" alt="Logo Avada Food">
        <div v-for="(link, index) in linkLeft" :key="index"  class="lefticons">  
          <i :class="link.icon"></i>
        </div> 
      </div>
      <div class="center-left-footer">
        <div v-for="(link, index) in linkCL" :key="index"  class="centerleftFooter">
          <a :href="link.text">{{link.text}}</a>
        </div>
      </div>
      <div class="center-right-footer">
        <div class="contact">
          <h5>CONTACT</h5>
          <h5><i class="fas fa-map-marker-alt"></i> 775 New York Ave, Brooklyn, Kings, New York 11203</h5>
          <h5><i class="fas fa-phone"></i> + 0100-505-0000</h5>
          <h5><i class="fas fa-envelope"></i> info@your-domain.com</h5>
        </div>
      </div>
      <div class="right-footer">
        <div class="app">
          <h5>GET OUR APP!</h5>
          <img src="../assets/img/download-android.png" alt="First Download">
          <img src="../assets/img/download-app-store.png" alt="Second Download">
        </div>
      </div>
    </div>
    <div class="bottom-footer">
      <h5>© Copyright 2012 - 2020 | Avada Theme by ThemeFusion | All Rights Reserved | Powered by WordPress</h5>
    </div>
  </footer>
</template>

<script>
import Link from '../assets/data/Link.js';
export default {
    name: 'Footer',
    data(){
      return{
        linkLeft: Link.leftFooter,
        linkCL: Link.centerleftFooter,
    }
  }
}
</script>

<style scoped lang="scss">
@import "../style/generals";
.container-small{
  display: flex;
  height: 300px;
  flex-direction: column;
  margin-top: 50px;
  
  .top-footer{
    display: flex;
    justify-content: flex-start;
    width: 100%;
    height: 250px;

    .left-footer{
    width: calc(100% / 4);
    height: 100%;

      img{
        width: 70%;
        display: block;
        margin-bottom: 10px;
        cursor: pointer;
      }

      .lefticons{
        display: inline-block;
        margin: 10px;
        color: $mediam-cut-5;
        cursor: pointer;
      }
    }

    .center-left-footer{
      width: calc(100% / 4);
      height: 100%;
      display: flex;
      flex-direction: column;

      .centerleftFooter{
        width: 100%;
        height: 100%;

        a{
          width: 100%;
          height: calc(100% / 5);
          text-decoration: none;
          color: black;
          font-weight: 600;
        }
      }
    }

    .center-right-footer{
      width: calc(100% / 4);
      height: 100%;
      display: flex;
      flex-direction: column;
      
      .contact{
        width: 100%;
        height: calc(100% / 5);
        color: $mediam-cut-5;
        cursor: pointer;
      }

      h5:first-child{
        margin-bottom: 20px;
        color: $color-cube-5;
      }

      h5{
        margin-bottom: 10px;
      }
    }

    .right-footer{
      width: calc(100% / 4);
      height: 100%;
      display: flex;
      flex-direction: column;

      h5{
        margin-bottom: 20px;
        color: $color-cube-5;
      }

      img{
        width: 100%;
        margin-bottom: 10px;
      }
    }
  }
  .bottom-footer{
    width: 100%;
    height: 50px;
    text-align: center;

    h5{
      margin-top: 20px;
      color: $mediam-cut-5;
    }
  }
}
</style>