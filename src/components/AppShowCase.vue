<script >
import FoodCardItem from './FoodCardItem.vue';

export default{
    name:"AppShowCase",

    components:{
        FoodCardItem
    },

    data(){
        return{
        
            shopNavLinks:["All Product", "Apple", "Food", "Orange", "Vegetable"],


            foods:[

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
                {
                    image:"./public/assets/showcaseImage/s4.jpg",
                    name:"Fresh Blueberries",
                    price:19,
                    sale:true,
                    salePrice:14,
                },
                {
                    image:"./public/assets/showcaseImage/s10.jpg",
                    name:"Organic Letus",
                    price:23,
                    sale:false,
                    salePrice:null,
                },
                {
                    image:"./public/assets/showcaseImage/s9.jpg",
                    name:"Red Gajor",
                    price:29,
                    sale:true,
                    salePrice:28,
                },
                {
                    image:"./public/assets/showcaseImage/s7.jpg",
                    name:"Nega Pepper",
                    price:21,
                    sale:false,
                    salePrice:null,
                },

            ],

        }

    }
}

</script>

<template>

    <div class="my_container">

        <div id="show-case">

            <div class="title">
                <div v-for="title in 2" class="title-inner">
                    <div class="top-title my_primary_color">
                        Trending Online Store
                    </div>
                    <div class="company-name">
                        Gogrin all 
                        <span class="my_primary_color">Organic</span>
                        food
                    </div>
                </div>
            </div>


            <nav>

                <ul>
                    <li v-for="currentLink in shopNavLinks">{{ currentLink }}</li>
                </ul>

            </nav>


            <div id="grid">

                <div class="row row-cols-4">

                    <div v-for="currentFood in foods" class="col">
                        <FoodCardItem
                            :food="currentFood"    
                        >
                        </FoodCardItem>
                    </div>

                </div>

            </div>

            <div class="text-center">

                <div class="my_btn_big my_btn_primary">All product</div>

            </div>




        </div>

    </div>
    
</template>

<style lang="scss" scoped>
    @use "../style/variables.scss" as *;

    #show-case{
        background-image: url("/public/assets/bg/shop-bg-img.jpg");
        padding:70px 145px;
        color:white;


        .title{
            text-align: center;
            margin-bottom: 35px;

            .top-title{
                font-size:1.2em;
                font-weight: 600;
            }

            .company-name{
                text-transform: uppercase;
                font-size:2em;
                font-weight: bold;
            }
        }


        nav{

            ul{
                display: flex;
                justify-content: center;
                gap:30px;

                padding: 0;

                margin-bottom: 30px;
                
                list-style-type: none;
                
                li{
                    cursor:pointer;
                    user-select: none;
                }
            }

        }

        #grid{
            margin-bottom: 40px;
        }

    }


</style>
