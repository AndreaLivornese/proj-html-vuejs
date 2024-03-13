<script >

export default{
    name:"Members",

    data(){
        return{

            membersLogo:[
                "/public/assets/brands/brand1.png",
                "/public/assets/brands/brand2.png",
                "/public/assets/brands/brand3.png",
                "/public/assets/brands/brand1.png",
                "/public/assets/brands/brand4.png"
            ],

        }
        
          

    }
}

</script>

<template>

<div class="my_container">
    
    <div class="row justify-content-center ">
        <div class="col-10 row row-cols-5 align-items-center ">

            <div v-for="currentBrand in membersLogo" class="col brand-img">
                <img :src="currentBrand" alt="logo membro associato">
            </div>


        </div>
    </div>
    
</div>
    
    
</template>

<style lang="scss" scoped>
    @use "../style/variables.scss" as *;

    .my_container{
        padding: 20px 0;

        .brand-img{
            text-align: center;

            img{
                height: 100%;
            }
        }
        
    }


    

</style>
