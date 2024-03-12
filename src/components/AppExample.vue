<script >
import { registerRuntimeCompiler } from 'vue';


export default{
    name:"AppExample",

    data(){
        return{
        
        }

    }
    
}

</script>

<template>


    <div class="my_container">
        
        <div class="row g-0 justify-content-center ">
            <div class="col-5">
                <h2>
                    <span class="my_primary_color">
                        Look what
                    </span>
                    consumer power has done with
                    <span class="my_primary_color">
                        organic food;
                    </span>
                    we can do the same with clothes.
                </h2>
            </div>
            <div class="col-5">
                <p>
                    I have a need to make these sorts of connections literal sometimes, and a vehicle often helps to do that, I have a reletionship to hosting culture,
                    <span class="my_primary_color">
                        It isn't really about it helps to do that, I have a relationship to hosting culture.
                    </span>
                </p>

                <p>
                    I have a need to make these sorts of connections literal sometimes, and a vehicle often helps to do that, I have a reletionship to hosting culture.
                </p>
            </div>
            <div class="col-10">

                <div class="row ">
                    <div class="col-3">
                        <img src="/public/assets/fe/fe1.jpg" alt="">
                    </div>
                    <div class="col-3">
                        <img src="/public/assets/fe/fe2.jpg" alt="">
                    </div>
                    <div class="col-3">
                        <img src="/public/assets/fe/fe3.jpg" alt="">
                    </div>
                    <div class="col-3">
                        <img src="/public/assets/fe/fe2.jpg" alt="">
                    </div>
                </div>

            </div>
        </div>

    </div>
   
  
</template>

<style lang="scss" scoped>
    @use "../style/variables.scss" as *;

    .my_container{
        padding:75px 0;
    }


    h2{
        color:$secondaryColor;
    }

    p{
        font-size: .8em;
    }

    .col-3 > img{
        width: 100%;
    }
   

    

</style>
