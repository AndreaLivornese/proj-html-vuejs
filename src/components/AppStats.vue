<script >

export default{
    name:"AppStats",

    data(){
        return{
        

        }

    }
}

</script>

<template>

<div class="my_container">
    
    <div class="counter">

        <div class="stats">

            <div class="box">
                <div class="number">
                    29+
                </div>
                <div class="description">
                    Years of Experienced
                </div>
            </div>
            <img src="/public/assets/counter-shap1.png" alt="">

            <div class="box">
                <div class="number">
                    200+
                </div>
                <div class="description">
                    Everyday Online Delivery
                </div>
            </div>
            <img src="/public/assets/counter-shap1.png" alt="">

            <div class="box">
                <div class="number">
                    20K
                </div>
                <div class="description">
                    Client Satisfaction
                </div>
            </div>
            <img src="/public/assets/counter-shap1.png" alt="">

            <div class="box">
                <div class="number">
                    30+
                </div>
                <div class="description">
                    Award Winning
                </div>
            </div>
            

        </div>

    </div>

    
</div>
    
    
</template>

<style lang="scss" scoped>
    @use "../style/variables.scss" as *;

    .counter{
        background-image: url("/public/assets/bg/counter-bg.jpg");
        padding:40px 0;

        .stats{
            display: flex;
            justify-content: center;
            align-items: center;
            gap:15px;

            text-align: center;

            .number{
                color:$primaryColor;
                font-size:3em;
                font-weight: bold;
            }

            .description{
                color:white;
                font-weight: bold;

            }

        }
    }

   

</style>
