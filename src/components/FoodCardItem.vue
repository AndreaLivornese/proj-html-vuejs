<script >



export default{
    name:"FoodCardItem",

    props:{
        food: Object,
    },

    data(){
        return{



        }

    }
}

</script>

<template>
   
   <div class="my_card">

        <div v-show="food.sale==true" class="sale">
            Sale!
        </div>

        <div class="my_card-img">
            <img :src="food.image" alt="food image">

            <div class="tools">
                <div class="tool-wrapper">
                    <i class="fa-solid fa-heart"></i>
                </div>
                <div class="tool-wrapper">
                    <i class="fa-solid fa-cart-shopping"></i>
                </div>
                <div class="tool-wrapper">
                    <i class="fa-solid fa-eye"></i>
                </div>
            </div>
        </div>
        <div class="my_card-info">

            <div class="name">
                {{ food.name }}
            </div>

            <div class="price-box">
                <div class="price" :class="food.sale == true ? 'discount' : ''">
                    ${{ food.price }}
                </div>
                <div v-show="food.sale == true" class="price">
                    ${{ food.salePrice }}
                </div>
            </div>


        </div>

   </div>
    
</template>

<style lang="scss" scoped>
    @use "../style/variables.scss" as *;

.my_card{
    position: relative;

    

    .sale{
        position:absolute;

        top:6px;
        right:6px;

        display: inline-block;

        padding:5px 7px;

        text-transform: uppercase;
        background-color: $primaryColor;
        font-weight: 600;
        font-size:.7em;
    }


    .my_card-img{
        position:relative;

        img{
            width: 100%;
        }

        .tools{
            
            display:none;
            justify-content: center;
            gap:5px;

            position:absolute;
            left:0;
            bottom:15px;

            width: 100%;

            color:black;

            .tool-wrapper{
                display: flex;
                justify-content: center;
                align-items: center;

                width: 30px;
                height: 30px;

                border-radius: 50%;
                
                background-color: white;

                transition: background-color .3s, color .3s;

                cursor:pointer;

                &:hover{
                    background-color: $primaryColor;
                    color:white;
                }
                
            }
        }
    }

    .my_card-info{
        display: flex;
        flex-direction: column;
        align-items: center;
        row-gap:10px;

        .name{
            font-weight: bold;
        }

        .price-box{
            display: flex;
            gap:5px;

            .price{
                color:$primaryColor;
            }

            .discount{
                opacity:.5;
            }
        }

        
    }

}


.my_card:hover .tools{
    display: flex;
}
    

</style>
