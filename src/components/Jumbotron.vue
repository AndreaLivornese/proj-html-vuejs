<script >


export default{
    name:"Jumbotron",

    data(){
        return{

        }
        
          

    }
}

</script>

<template>

<div class="my_container">
    
    <div class="jumbotron">
        <img src="/public/assets/bg/call-to-bg.jpg" alt="sfondo jumbotron">

        <div id="jumbo-inner">
            <div class="top-title">
                Here you can get 100% fresh organic food
            </div>

            <h3>
                Best prganic food up to 25% off for all product
            </h3>

            <p>
                The most beautiful people we have known are those who have known defeat, known suffering, known struggle, known loss, and have found their way out of those depths. The most beautiful people we have known are those who have khnow defeat, known suffering.
            </p>


            <div class="d-flex justify-content-center gap-4">
    
                <div class="jumbo-btn my_btn_primary">
                    +393396082435
                </div>
    
                <div class="jumbo-btn my_btn_secondary">
                    apoinment
                </div>
    
            </div>
        </div>

    </div>
    
</div>
    
    
</template>

<style lang="scss" scoped>
    @use "../style/variables.scss" as *;


.jumbotron{
    position:relative;

    img{
        width: 100%;
    }

    #jumbo-inner{
        position:absolute;
        top:50%;
        left:50%;
        transform:  translate(-50%, -50%);

        text-align: center;

        color:white;

        .top-title, h3{
            font-weight: bold;
            margin-bottom: 18px;
        }

    

        h3{
            font-size:2em;
        }

        p{
            font-size: .8em;
            font-weight: 500;
            margin-bottom: 24px;
        }
    }

    .jumbo-btn{
        display: inline-block;
        padding:12px 22px;

        cursor:pointer;
        user-select: none;

        text-transform: uppercase;
        text-decoration: none;

        font-size:.8em;
    }
}


</style>
