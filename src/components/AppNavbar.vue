<script >

export default{
    name:"AppNav",

    data(){
        return{
          
            linksMenu:[

                {
                    title:"Home",
                    subMenuLinks:[
                        
                    ]
                },
                {
                    title:"Abount",
                    subMenuLinks:[
                        
                    ]
                },
                {
                    title:"Service",
                    subMenuLinks:[
                        
                    ]
                },
                {
                    title:"Portfolio",
                    subMenuLinks:[
                        
                    ]
                },
                {
                    title:"Shop",
                    subMenuLinks:[
                        
                    ]
                },
                {
                    title:"Blog",
                    subMenuLinks:[
                        
                    ]
                },
                {
                    title:"Contact",
                    subMenuLinks:[
                        
                    ]
                },

            ]

        }

    }
}

</script>

<template>

   <nav>
        <div class="container">
            
            <div id="nav-inner">

                <div id="nav-left">
                    <div class="logo">
                        <img src="/public/assets/logo/logo.png" alt="logo azienda">
                    </div>

                    <div class="links">
                        <ul>
                            <!-- fixare le icone -->
                            <li v-for="currentLink in linksMenu" >{{ currentLink.title }}<i class="fa-solid fa-chevron-down"></i></li>
                        </ul>
                    </div>
                </div>

                <div id="nav-right">
                    <div class="search">
                        cerca
                    </div>
                    <div class="shopping-cart">
                        carrfello
                    </div>
                    <div class="order">
                        <a class="btn btn-primary">order now</a>
                    </div>
                </div>

            </div>

        </div>
   </nav>
  
</template>

<style lang="scss">
    @use "../style/variables.scss" as *;
    @use '../style/general.scss' as *;


    nav{
        padding: 12px 0;


        #nav-inner{
            display: flex;
            justify-content: space-between;
            align-items: center;

            #nav-left, #nav-right{
                display: flex;
                align-items: center;
                
            }

            #nav-left{
                gap:65px;
            }

            #nav-right{
                gap:15px;
            }


            .links ul{
                display: flex;
                gap:15px;

                padding: 0;
                list-style-type: none;
            }

        }
    }

</style>
