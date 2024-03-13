<script >


export default{
    name:"NewsItem",

    props:{
        news:Object,
    },

    data(){
        return{

        }
    }
}

</script>

<template>

<div class="news">

    <div class="news-img">
        <img :src="news.image" alt="immagine della notizia">
    </div>
    <div class="news-info">
        <div class="creator">
            {{ news.creator }}
        </div>
        <div class="news-date">
            {{ news.date }}
        </div>

    </div>
    <div class="news-text">
        <h3 class="news-title">
            {{ news.title }}
        </h3>
        <div class="news-article">
            {{ news.text }}
        </div>

    </div>
    <div class="more">
        Read more...
    </div>
    
    

</div>
    
    
</template>

<style lang="scss" scoped>
    // @use "../style/variables.scss" as *;
    @use "../style/general.scss" as *;


    .news{
        display: flex;
        flex-direction: column;

        .news-img{
            @include mb-news; 
        
            img{
            display: block;
            width: 100%;
            }
        }

        .news-info{
            display: flex;
            gap:10px;

            color:#888888;
            font-size:.8em;
            @include mb-news;

        }

        .news-text{
            @include mb-news;

            h3{
                font-size: 1.2em;
                color:$secondaryColor;
                font-weight: bold;
            }

            .news-article{
                font-size:.9em;
                line-height: 1.7em;
                color:#888888;
            }

        }

        .more{
            color:$secondaryColor;
            text-transform: uppercase;
            font-weight: 500;
        }
    }


</style>
