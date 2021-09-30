<template>
    <div class="container-large">
        <div class="banner">
            <div class="text">
                <div>TODAY'S PICK</div>
                <h1>Food Corner: Top Japanese Restourants for Sushi</h1>
                <h5>March 25, 2019</h5>
            </div>
        </div>
        <div class="container-small">
            <div class="height-10"></div>
            <h3 class="color-cut-1">FOODIE JOURNAL</h3>
            <div class="three-images">
                <div>
                    <img src="../assets/img/banner.jpg" alt="">
                    <h3 class="text-image">Food corner: Top Japanese Restaurants for Sushi</h3>
                    <h5>By admind 1 March 35th, 2019</h5>
                </div>
                <div>
                    <img src="../assets/img/fi-roundup.jpg" alt="">
                    <h3 class="text-image">Roundup: My New Favourite Repices For Healthy Living</h3>
                    <h5>By admind 1 March 35th, 2019</h5>
                </div>
                <div>
                    <img src="../assets/img/fi-toasts.jpg" alt="">
                    <h3 class="text-image">Why These Toasts with Tea are My New Favourite</h3>
                    <h5>By admind 1 March 35th, 2019</h5>
                </div>    
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
.container-large{
    height: 100%;      

    //inizio banner
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
    //fine banner
    //inizio foodie journal
    .container-small{
        height: 400px;
        background-color: $color-cube-1;
        text-align: center;
        transform: translate(0, -15%);

        .height-10{
            height: 10px;
        }

        .color-cut-1{
            color: $mediam-cut-1;
        }

        .three-images{
            display: flex;
            justify-content: space-around;
            
            img{
                width: 300px;
                height: 170px;
                margin: 20px 0;
            }
            .text-image{
                width: 70%;
                margin: 0 auto;
                color: $mediam-cut-1;
            }
            h5{
                margin-top: 10px;
                color: $mediam-cut-5;
            }
        }
    }
}

</style>