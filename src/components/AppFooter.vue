<script >

export default{
    name:"AppFooter",

    data(){
        return{

            footerLink:{
                title:"Emergency Link.",
                links:[
                    "Organic Food Shop",
                    "Our Teem & Condition.",
                    "Gogrin Faq Section",
                    "Our Team Member",
                    "Our Latest News Feed"
                ]
            },

            footerBlog:{
                title:"Our Latest Blog.",

                blogs:[
                    {
                        img:"/public/assets/footerImg/blo1-100x100.jpg",
                        text:"Where I live, I am surrending by fresh, organics food, so I eat really well.",
                        date:"December 17, 2022"
                    },
                    {
                        img:"/public/assets/footerImg/blo2-100x100.jpg",
                        text:"What we get at home is 100% organic food. We are also 90% vegetarian.",
                        date:"December 16, 2022"
                    },
                ],
                
                
            },

            gallery:{
                title:"Our Gallery",
                images:[
                    "/public/assets/footerImg/blo1-100x100.jpg",
                    "/public/assets/footerImg/blo7-100x100.jpg",
                    "/public/assets/footerImg/blo3-100x100.jpg",
                    "/public/assets/footerImg/blo4-100x100.jpg",
                    "/public/assets/footerImg/blo8-100x100.jpg",
                    "/public/assets/footerImg/blo9-100x100.jpg"
                ]
            },
                
            

        }
        
          

    }
}

</script>

<template>

<div class="my_container">

    <footer>

        <div class="row justify-content-center ">

            <div class="col-10 row" id="footer-inner">
                
                <div class="footer-social col-3">
                    <img src="/public/assets/logo/footer-logo.png" alt="logo">
                    <p>
                        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Eos esse odio.
                    </p>

                    <ul class="social-logo">
                        <li><i class="fa-brands fa-facebook-f"></i>a</li>
                        <li><i class="fa-brands fa-google-plus-g"></i>b</li>
                        <li><i class="fa-brands fa-twitter"></i>c</li>
                        <li><i class="fa-brands fa-pinterest-p"></i>d</li>
                    </ul>
                </div>

                <div class="footer-links col-2">
                    <h3>{{ footerLink.title }}</h3>
                    <ul class="column">
                        <li v-for="currentLink in footerLink.links">
                            <a href="">{{ currentLink }}</a>
                        </li>
                    </ul>   
                </div>

                <div class="last-blog col-4">
                    <h3>{{ footerBlog.title }}</h3>

                    
                    <div class="card-container">
                        <div v-for="currentBlog in footerBlog.blogs" class="my_card">
                            <img :src="currentBlog.img" alt="">
                            <div class="card-text">
    
                                <div class="text">
                                    {{ currentBlog.text }}
                                </div>
                                <div class="date">
                                    {{ currentBlog.date }}
                                </div>
    
                            </div>
                        </div>
                    </div>

                </div>

                <div class="gallery col-3">
                    <h3>{{ gallery.title }}</h3>

                    <div class="row row-cols-3 row-gap-3">
                        <div v-for="currentImg in gallery.images" class="col">
                            <img :src="currentImg" alt="immagine della galleria">
                        </div>
                    </div>

                </div>
    
    
            </div>

        </div>

    </footer>
    
    
</div>
    
    
</template>

<style lang="scss" scoped>
    @use "../style/variables.scss" as *;



    footer{
        background-image: url(/public/assets/bg/footer-bg.jpg);

        padding:105px 0 55px;

        ul{
            list-style-type: none;
            padding: 0;
            display: flex;
        }

        h3{
            color:white;
            font-weight: bold;
            font-size: 1.3em;

            margin-bottom: 22px;
        }

        .column{
            flex-direction: column;
            gap:14px;

            a{
                text-decoration: none;
                color:white;
                font-weight: 500;
                font-size:.8em
            }
        }

        #footer-inner{


            .footer-social{
                display: flex;
                flex-direction: column;
                align-items: flex-start;
                gap:16px;

                img{
                    width: initial;
                }

                p{
                    margin: 0;
                    color:white;
                    font-weight: 500;
                    font-size: .8em;
                }

                .social-logo{
                    gap:16px;
                }
            }

            .last-blog{


                .card-container{
                    display: flex;
                    flex-direction: column;
                    gap:16px;

                }

                .my_card{
                    display: flex;
                    color:white;

                    img{
                        width: 80px;
                        height: 80px;      
                    }

                    .text{
                        font-weight: 500;
                    }

                    .date{
                        font-size: 0.8em;
                    }
                }
            }


            .gallery{
                img{
                    width: 100%;
                }
            }
        }

        
    }


   

</style>
