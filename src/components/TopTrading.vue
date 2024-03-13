<script >
import TopFoodCardItem from './TopFoodCardItem.vue';

export default{
    name:"TopTrading",

    components:{
        TopFoodCardItem,
    },

    data(){
        return{
        
            topFoods:[
                {
                    image:"./public/assets/showcaseImage/s5.jpg",
                    name:"Fress Apple",
                    price:18,
                    sale:false,
                    salePrice:null,
                },
                {
                    image:"./public/assets/showcaseImage/s2.jpg",
                    name:"Fress Cobies",
                    price:18,
                    sale: true,
                    salePrice:17,
                },
                {
                    image:"./public/assets/showcaseImage/s8.jpg",
                    name:"Fresh Waterlemon",
                    price:15,
                    sale:false,
                    salePrice:null,
                },
                {
                    image:"./public/assets/showcaseImage/s1.jpg",
                    name:"Organic Juice",
                    price:20,
                    sale:true,
                    salePrice:15,
                },
            ]

        }

    }
}

</script>

<template>

<div class="my_container">
    
    <div id="title">
        <div id="top-title">
            Running week top selling
        </div>
        <h2>
            Top 
            <span class="my_primary_color">
                Treding
            </span>
            organic food
        </h2>
    </div>

    <div id="grid">
        <div class="col-10">
            <div class="row row-cols-4">
                <div v-for="currentFood in topFoods" class="col">
                    <TopFoodCardItem
                        :food="currentFood"
                    >
                    </TopFoodCardItem>
                </div>
            </div>
        </div>
    </div>

    
</div>
    
    
</template>

<style lang="scss" scoped>
    @use "../style/variables.scss" as *;
    @use "../style/general.scss" as *;


    .my_container{
        padding:45px 0 68px;

        #title{
           @include title;

            #top-title{
                @include top-title;
            }

            h2{
                @include h2;
            }
        
        }

        #grid{
            display: flex;
            justify-content: center;
        }
    }

    
</style>
