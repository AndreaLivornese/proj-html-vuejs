<script >

export default{
    name:"AppNav",

    data(){
        return{
          
            linksMenu:[

                {
                    title:"Home",
                    subMenuLinks:[
                        "Home", "Home", "Home"
                    ]
                },
                {
                    title:"Abount",
                    subMenuLinks:[
                        "About","About","About",
                    ]
                },
                {
                    title:"Service",
                    subMenuLinks:[
                        "Service","Service","Service"
                    ]
                },
                {
                    title:"Portfolio",
                    subMenuLinks:[
                        "Portfolio","Portfolio","Portfolio"
                    ]
                },
                {
                    title:"Shop",
                    subMenuLinks:[
                    "Shop","Shop","Shop"
                    ]
                },
                {
                    title:"Blog",
                    subMenuLinks:[
                    "Blog","Blog","Blog"
                    ]
                },
                {
                    title:"Contact",
                    subMenuLinks:[
                    "Contact","Contact","Contact"
                    ]
                },

            ],

            indexMenu:null,

        }

    },
    methods:{

        activeMenu(index){
            this.indexMenu = index;
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

                    
                    <ul class="nav-links">
                        <!-- fixare le icone -->
                        <li v-for="(currentLink, index) in linksMenu" @click="activeMenu(index)">
                            {{ currentLink.title }}
                            <i class="fa-solid fa-chevron-down"></i>

                            <div v-show="index == indexMenu" class="menu">

                                <ul class="menu-links">
                                    <li v-for="currentLinkMenu in currentLink.subMenuLinks">{{ currentLinkMenu }}</li>
                                </ul>

                            </div>
                        </li>
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

                .nav-links{
                    display: flex;
                    gap:20px;
    
                    padding: 0;
                    margin: 0;

                    list-style-type: none;

                    cursor:pointer;
                    user-select: none;

                    &>li{
                        position:relative;
                        display: flex;
                        align-items: center;
                        gap:3px;
                        
                        i{
                            font-size:.6em
                        }

                        .menu{
                            width: 100px;
                            
                            position:absolute;
                            left:0;
                            bottom:-152px;
                            z-index: 1;

                            background-color: white;

                            box-shadow: 0px -3px 5px #888888;

                            padding:20px;

                            .menu-links{
                                padding: 0;
                                margin: 0;

                                list-style-type: none;

                                line-height: 1.8em;
                            }

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
