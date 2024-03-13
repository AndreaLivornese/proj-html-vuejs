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
        <div class="my_container">
            
            <div id="nav-inner">

                <div id="nav-left">
                    <div class="logo">
                        <img src="/public/assets/logo/logo.png" alt="logo azienda">
                    </div>

                    
                    <ul>
                        <!-- fixare le icone -->
                        <li v-for="currentLink in linksMenu" >{{ currentLink.title }}<i class="fa-solid fa-chevron-down"></i></li>
                    </ul>
                  
                </div>

                <div id="nav-right">
                    <div class="search">
                        <i class="fa-solid fa-magnifying-glass"></i>
                    </div>
                    <div class="shopping-cart">
                        <i class="fa-solid fa-cart-shopping"></i>
                    </div>
                    <div class="order">
                        <a class="my_btn my_btn_primary">order now</a>
                    </div>
                </div>

            </div>

        </div>
   </nav>
  
</template>

<style lang="scss" scoped>
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
                align-items: center;
                gap:65px;

                ul{
                    display: flex;
                    gap:20px;
    
                    padding: 0;
                    margin: 0;
                    list-style-type: none;

                    cursor:pointer;
                    user-select: none;

                    li{
                        display: flex;
                        align-items: center;
                        gap:3px;
                        
                        i{
                            font-size:.6em
                        }
                    }
                }
            }

            #nav-right{
                gap:15px;

                .search{
                    display: flex;
                    justify-content: center;
                    align-items: center;

                    width: 30px;
                    height: 30px;

                    border-radius: 50%;

                    text-align: center;
                    color:white;
                    background-color: $primaryColor;
                }

                .shopping-cart{
                    color:$secondaryColor;
                }
            }



        }
    }

</style>
