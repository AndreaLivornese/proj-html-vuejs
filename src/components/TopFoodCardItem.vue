<script >

export default{
    name:"TopFoodCardItem",

    props:{
        food:Object,
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
        </div>
        <div class="my_card-info">

            <div class="name">
                {{ food.name }}
            </div>
            <div class="price">
                {{ food.price }}
            </div>

        </div>

    </div>
    
    
</template>

<style lang="scss" scoped>
    @use "../style/variables.scss" as *;


    .my_card{
    position: relative;

    box-shadow: 0 0 10px #d1d0d0;

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
            color:white;
        }


        .my_card-img{
            margin-bottom: 35px;

            img{
                width: 100%;
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

            .price{
                color:#888888;
            }
            
        }
    }

    
</style>
