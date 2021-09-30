<template>
  <div class="container">
    <div class="banner">
        <div class="text">
            <div>TODAY'S PICK</div>
            <h1>Food Corner: Top Japanese Restourants for Sushi</h1>
            <h5>March 25, 2019</h5>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Main',
}
</script>

<style scoped lang="scss">
@import "../style/generals";
.container{
    width: 90%;
    height: 100%;      

    .banner{
        display: flex;
        justify-content: center;
        align-items: center;
        background-image: url("../assets/img/banner.jpg");
        height: 550px;
        width: 100%;
        background-size: cover;
        background-position: center;

        .text{
            width: 500px;
            height: 150px;
            background-color: $color-cube-1;    
            position: absolute;
            text-align: center;

            div{
                height: 30px;
                width: 150px;
                line-height: 30px;
                align-items: center;
                background-color: $color-cube-5;
                border-radius: 5px;
                transform: translate(120%, -50%);
                color: $mediam-cut-2;
            }

            h1{
                color: $mediam-cut-1;
            }

            h5{
                margin-top: 20px;
                color: $mediam-cut-5;
            }
        }
    }
    
}

</style>