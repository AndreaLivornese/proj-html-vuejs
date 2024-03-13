<script >

export default{
    name:"Citation",

    data(){
        return{
        

        }

    }
}

</script>

<template>

<div class="my_container">
    
    <div class="citation text-center">
        <div class="img-title">
            <!-- da fixare l'icona -->
            <i class="fa-solid fa-quote-left"></i>
        </div>

        <p>
            "Dessert pudding dessert jelly beans cupcake sweet caramels gingerbread. Fruitcake bisquit cheesecake. Cookie topping sweets muffine pudding tart bear claw sugar plum croissant.". We started as a small legal consultacy. We have proved our competence and had many satisfied clients.
        </p>

        <div class="person">
            Martha Alex
        </div>
        <div class="role my_primary_color">
            Manager
        </div>
    </div>
    
</div>
    
    
</template>

<style lang="scss" scoped>
    @use "../style/variables.scss" as *;

   .citation{
    display: flex;
    flex-direction: column;
    align-items: center;

    padding:70px 214px 60px;

    .img-title{
        font-size: 60px;
        color: $secondaryColor;

    }

    p{
        font-size:1.1em;
        color:#1d2055;
        font-weight: 500;
    }

    .person{
        font-weight: bold;
    }
    .role{
        font-weight: bold;
        font-size: .8em;
    }
   }


</style>
