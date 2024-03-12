<script >
import { registerRuntimeCompiler } from 'vue';


export default{
    name:"AppSlider",

    data(){
        return{
        
            images:[
                "H3-slider3.jpg", "slider.jpg"
            ],

            indexImage:0,

        }

    },
    methods:{

        moveRightImge(){


                if(this.indexImage == this.images.length -1){
                    this.indexImage = 0;
                }else{
                    this.indexImage++;
                }
        },

        moveLeftImage(){
            
            if(this.indexImage == 0){
                    this.indexImage = this.images.length -1
                }else{
                    this.indexImage--
            }
        }



    }
}

</script>

<template>

    <div id="slider">
        <img 
            v-for="(currentImage,index) in images"
            :src="'/public/assets/slider/'+currentImage" 
            v-show="index == indexImage"
            alt="immagine slider"
        >

        <div id="arrows">
            <i class="fa-solid fa-chevron-left" @click="moveLeftImage"><</i>
            <i class="fa-solid fa-chevron-right" @click="moveRightImge">></i>
        </div>

        <div id="slider-text">

            <h1>
                Gorgrin organic food
            </h1>
            
            <div id="slogan">
                <div>
                    Eating naturally & organic is always be healty
                </div>
            </div>

            <div id="about-company">
                <a class="my_btn_big my_btn_primary" href="#">About us</a>
                <a class="my_btn_big my_btn_secondary" href="#">Our history</a>
            </div>

        </div>
    </div>
  
</template>

<style lang="scss">
    @use "../style/variables.scss" as *;

    #slider{
        position:relative;

        height: 800px;
        overflow: hidden;

        img{
            display: block;
            width: 100%;
            
        }
        
        #arrows{
            position: absolute;
            top:0;
            left:0;
            z-index: 1;

            width: 100%;
            height: 100%;

            display: flex;
            justify-content: space-between;
            align-items: center;

            &>i{
                cursor:pointer;
                user-select: none;
            }
        }

        #slider-text{
            position: absolute;
            top:50%;
            left:50%;
            transform: translate(-50%,-50%);
            z-index: 1;

            text-align: center;
            color:white;



            h1{
                font-size:15px;
                text-transform: uppercase;
                font-weight: 600;
            }


            #slogan{

                margin-bottom: 40px;
                
                &>div{
                    font-size: 60px;
                    font-weight: bold;
                }
            }


            #about-company{
                display: flex;
                justify-content: center;

                gap:15px;

            }


        }
    }

    

</style>
