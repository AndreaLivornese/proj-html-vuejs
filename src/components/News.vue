<script >
import NewsItem from './NewsItem.vue';

export default{
    name:"News",

    components:{
        NewsItem
    },

    data(){
        return{

            news:[

                {
                    image:"/public/assets/news/blo1-390x250.jpg",
                    creator:"Gogrin",
                    date:"17 dec 2022",
                    title:"Where I live, I am surrounded by fresh, organic food, so I eat really well.",
                    text:"Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ad ut voluptatibus placeat maiores id fugiat, sunt sit voluptates libero quia.",
                },
                {
                    image:"/public/assets/news/blo2-390x250.jpg",
                    creator:"Gogrin",
                    date:"18 dec 2022",
                    title:"What we get at home is 100% organic food. We are also 90% vegetarian.",
                    text:"Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ad ut voluptatibus placeat maiores id fugiat, sunt sit voluptates libero quia.",
                },
                {
                    image:"/public/assets/news/blo3-390x250.jpg",
                    creator:"Gogrin",
                    date:"15 dec 2022",
                    title:"If we as a society are willing to have a preference for organic food farmer",
                    text:"Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ad ut voluptatibus placeat maiores id fugiat, sunt sit voluptates libero quia.",
                },

            ],

        }
        
          

    }
}

</script>

<template>

<div class="my_container">
    
    <div id="title">
        <div id="top-title">
            The news what we have
        </div>
        <h2>
            gogrin latest
            <span class="my_primary_color">
                news
            </span>
            feed
        </h2>
    </div>

    <div class="row justify-content-center ">
        <div class="col-10 row row-cols-3">

            <div v-for="currentNews in news" class="col">
                <NewsItem
                    :news="currentNews"
                >
                </NewsItem>
            </div>


        </div>
    </div>

</div>
    
    
</template>

<style lang="scss" scoped>
    @use "../style/variables.scss" as *;
    @use "../style/general.scss" as *;


    .my_container{
        padding:40px 0;
        
        #title{
               @include title;
    
                #top-title{
                    @include top-title;
                }
    
                h2{
                    @include h2;
                }
        }
    }


</style>
