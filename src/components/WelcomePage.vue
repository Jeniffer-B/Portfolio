<template>
    <div class="container">
        <div class="bgContainer">
            <div class="text-wrapper">
                <div class="hello">
                    Hello!
                </div>
                <div class="name">
                    I'm Jeniffer Beltrán
                </div>
                <div class="profession">
                    Junior Frontend developer
                </div>
            </div>
                <img class="homeImg" src="@/assets/homeImg.png" alt="homeImg">
        </div>
    </div> 
</template>
<script>
export default {
    name: 'Home'
}
</script>
<style scoped>
.container {
    display: flex;
    justify-content: center;
    align-items: center;
}
.bgContainer{
    height:100vh;
    width: 100%;
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    background-color: #393E41;
}
.text-wrapper{
    text-align: left;
    font-family: 'Quantico', sans-serif;
    letter-spacing: 0.2em;
    width: 40%;
}
.text-wrapper div {
    padding: 0.5em;
}
.hello{
    color: #FAB099;
    font-size: 3em;
}
.name{
    color: #B97CA2;
    font-size: 3em;
}
.profession{
    color: #B97CA2;
    font-size: 1.5em;
}
.homeImg{
    width: 40%;
}
    /*Escritorio*/
@media (min-width: 1199.98px) {
   
}
/* tablet */
@media (min-width: 576px) and (max-width: 991.98px) and (orientation:portrait) {
    .bgContainer{
        flex-direction: column;
    }
    .text-wrapper{
        width: 90%;
    }
    .text-wrapper div {
         padding: 0.5em;
    }
    .profession{
        font-size: 1.2em;
    }
    .homeImg{
        width: 25%;
        height: 15%;
    }
    .text-wrapper{
        width: 90%;
    }
    .text-wrapper div {
        padding: 0.7em;
    }
    .hello{
        font-size: 3em;
    }
    .name{
        font-size: 2.5em;
    }
    .profession{
        font-size: 1.5em;
    }
    .homeImg{
        width: 40%;
    }
}
@media (min-width: 991.98px) and (max-width: 1199.98px)and (orientation:landscape) {
    .bgContainer{
        justify-content: space-around;
    }
    .text-wrapper{
        width: 80%;
    }
}
/*movil*/
@media (max-width: 575.98px)and (orientation:portrait) {
    .bgContainer {
        flex-direction: column;
    }
    .text-wrapper{
        width: 90%;
    }
    .text-wrapper div {
        padding: 0.3em;
    }
    .hello{
        font-size: 1.5em;
    }
    .name{
        font-size: 1.4em;
    }
    .profession{
        font-size: 1em;
    }
    .homeImg{
        width: 45%;
    }
}
@media (min-width: 576px) and (max-width: 991.98px) and (orientation:landscape) {
    .hello{
        font-size: 1.5em;
    }
    .name{
        font-size: 1.4em;
    }
    .profession{
        font-size: 0.8em;
    }
    .homeImg{
        width: 30%;
    }
}
</style>
