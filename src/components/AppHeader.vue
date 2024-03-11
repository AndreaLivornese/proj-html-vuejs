<script >

export default{
    name:"AppHeader",

    data(){
        return{
          
            position: "North baukhula, tala , USA",
            email: "deco@example.com",

            timeWork: "8:30AM-8:30PM",

        }

    }
}

</script>

<template>

    <Header>

        <div class="container">
            
            <div id="inner-header">
                <div class="info">
                    <div id="position">
                        {{ position }}
                    </div>
                    <div id="email">
                        {{ email }}
                    </div>
                </div>

                <div class="info">
                    <div id="work-time">
                        {{ timeWork }}
                    </div>
                    <div id="header-social">
                        social
                    </div>

                </div>
            </div>

        </div>

    </Header>
  
</template>

<style lang="scss">
    @use "../style/variables.scss" as *;

    header{
        padding:10px 0;

        background-color: $primaryColor;
        color:white;

        font-size: 10px;
    }

    #inner-header{
        display:flex;
        justify-content: space-between;

        .info{
            display: flex;
            gap:30px;
        }

    }


</style>
