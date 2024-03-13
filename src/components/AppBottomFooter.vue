<script >

export default{
    name:"AppBottomFooter",

    data(){
        return{


        }
        
          

    }
}

</script>

<template>

<div class="footer-bottom">
    <div class="my_container">
        
        <div class="row justify-content-center ">

            <div class="col-10 inner-footer-bottom" >
                <div class="copyright">
                    Copyright 

                    googrin all rights reserved.
                </div>

                <ul class="links">
                    <li><a href="">Service</a></li>
                    <li><a href="">Pricing Table</a></li>
                    <li><a href="">Contact</a></li>
                </ul>
            </div>

        </div>

    </div>

</div class="footer-bottom">
    
    
</template>

<style lang="scss" scoped>
    @use "../style/variables.scss" as *;

    .footer-bottom{
        background-color: $secondaryColor;


        .inner-footer-bottom{
            display: flex;
            justify-content: space-between;
            align-items: center;

            padding:20px 0;

            color:white;
            font-size:0.8em;

            ul{
                display: flex;
                gap:15px;
                padding: 0;
                margin: 0;
                list-style-type: none;

                a{
                    color:white;
                    text-decoration: none;
                    user-select: none;
                }
            }
        }
    }


   

</style>
