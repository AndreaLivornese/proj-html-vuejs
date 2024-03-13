<script >

export default{
    name:"NewsLatters",

    data(){
        return{

        }
        
          

    }
}

</script>

<template>

<div class="my_container">
    
    <div class="row justify-content-center ">
        
        
        <div class="col-10 d-flex align-items-center "id="newsletter">

            <div class="col-6 text-center">
                <strong>
                    Subscribe our newsletter
                </strong>
            </div>

            <div class="col-6">
                <form>

                    <div class="my_input_group">
                        <input type="text" placeholder="your email" class="my_input">
                        <input type="button" class="newsletter-input-btn my_btn_secondary" value="Send">
                    </div>



                </form>
            </div>
    
        </div>

    </div>
    
</div>
    
    
</template>

<style lang="scss" scoped>
    @use "../style/variables.scss" as *;


    #newsletter{
        background-image: url(/public/assets/bg/milesim-bg.jpg);

        padding:26px 26px;


        strong{
            font-size:1.5em;
            text-transform: uppercase;
            color:white;
        }

        .my_input_group{
            display: flex;
            

            .my_input{
                flex-grow: 1;

                padding: 0 16px;
            }

            .newsletter-input-btn{
                padding:12px 35px;

                border:none;
                text-transform: uppercase;
                font-size:.9em;
                font-weight: 500;
            }

        }
    }

</style>
