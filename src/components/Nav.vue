<template>
    <div>
        <div id="nav">
            <router-link to="/">
                <div class="iconDiv">
                    <img src="@/assets/icons/homeIcon.png" alt="home Icon">
                    <p>Home</p>
                </div>
            </router-link>
            <router-link to="/about">
                <div class="iconDiv">
                    <img src="@/assets/icons/about.png" alt="about Icon">
                    <p>about</p>
                </div>
            </router-link>
            <router-link to="/projects">
                <div class="iconDiv">
                    <img src="@/assets/icons/codeIcon.png" alt="projects Icon">
                    <p>Projects</p>
            </div>
            </router-link>
            <router-link to="/contact">
                <div class="iconDiv">
                    <img src="@/assets/icons/contactIcon.png" alt="contact Icon">
                    <p>Contact</p>
                </div>
            </router-link>
        </div>

        <section id="banner">
            <input type="checkbox" id="menu--toggle">
            <label for="menu--toggle" id="trigger"></label>
            <label for="menu--toggle" id="burger"></label>
            <ul id="menu">
                <li><router-link to="/">
                <div class="iconDiv">
                    <img src="@/assets/icons/homeIcon.png" alt="home Icon">
                    <p>Home</p>
                </div>
                </router-link></li>
                <li><router-link to="/about">
                <div class="iconDiv">
                    <img src="@/assets/icons/about.png" alt="about Icon">
                    <p>about</p>
                </div>
            </router-link></li>
                <li>            <router-link to="/projects">
                <div class="iconDiv">
                    <img src="@/assets/icons/codeIcon.png" alt="projects Icon">
                    <p>Projects</p>
            </div>
            </router-link></li>
                <li><router-link to="/contact">
                <div class="iconDiv">
                    <img src="@/assets/icons/contactIcon.png" alt="contact Icon">
                    <p>Contact</p>
                </div>
            </router-link></li>
            </ul>  
        </section>

        <router-view/>
    </div>
</template>
<style>
#nav {
    padding: 0.5%;
    background-color: #393E41;
    display: flex;
    justify-content: center;
}
.iconDiv{
    margin: 1em;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    position: relative;
    margin: 20px 20px;
    width: 150px;
    height: 150px;
    border-radius: 75px;
    transition: 1s box-shadow;
}
.iconDiv p{
    color: #B97CA2;
    font-family: 'Quantico', sans-serif;
    text-decoration:none;
}
.iconDiv:hover {
    box-shadow: 0 5px 35px 0px #FAB099;
}
.iconDiv img{
    max-height: 65px;
}
/* hamburguer menu */
#trigger,
#burger,
#burger::before,
#burger::after {
    position: absolute;
    top: 25px;
    left: 25px;
    background: #B97CA2;
    width: 30px;
    height: 5px;
    transition: .2s ease;
    cursor: pointer;
    z-index: 1;
}
#trigger {
    height: 25px;
    background: none;
}
#burger::before {
    content: '';
    top: 10px;
    left: 0;
}
#burger::after {
    content: '';
    top: 20px;
    left: 0;
}
#menu--toggle:checked + #trigger + #burger {
    top: 35px;
    transform: rotate(180deg);
    transition: transform .2s ease;
}
#menu--toggle:checked + #trigger + #burger::before {
    width: 20px;
    top: -2px;
    left: 18px;
    transform: rotate(45deg) translateX(-5px);
    transition: transform .2s ease;
}
#menu--toggle:checked + #trigger + #burger::after {
    width: 20px; 
    transform: rotate(-45deg) translateX(20px);
    transition: transform .2s ease; 
}
#menu {
    position: absolute;
    margin: 0;
    padding: 0;
    width: 110px;
    height: 110px;
    background: #344A53;
    border-bottom-right-radius: 100%;
    box-shadow: 0 2px 5px #000;
    animation: not-checked-anim .2s both;
    transition: .2s;
    overflow: hidden;
}
#menu--toggle:checked + #trigger + #burger + #menu {
    animation: checked-anim 1s ease both;
}
#menu--toggle:checked + #trigger ~ #menu > li{
    display: block;
}
li {
    margin: 75px 0 -55px 0;
    text-decoration: none;
    list-style: none;
    outline: 0;
    display: none;
    width: 230px;
}
[type="checkbox"]:not(:checked),
[type="checkbox"]:checked {
    display: none;
}
@keyframes checked-anim {
    50% {
        width: 2000px;
        height: 2000px;
    }
    100% {
        width: 100%;
        height: 100%;
        border-radius: 0;
    }
}
@media (min-width: 1199.98px) {
    #banner {
        display: none;
    }   
}
/* tablet */
@media (min-width: 576px) and (max-width: 991.98px) and (orientation:portrait) {
    #banner {
        display: none;
    }
    .iconDiv img{
        max-height: 50px;
    }
}
@media (min-width: 991.98px) and (max-width: 1199.98px)and (orientation:landscape) {
  #banner {
        display: none;
    }
    .iconDiv{
        margin: 0.2em;
        margin: 10px 10px;
        width: 90px;
        height: 90px;
        border-radius: 50px;
        transition: 1s box-shadow;
    }
    .iconDiv img{
        max-height: 40px;
    }  
}
/*movil*/
@media (max-width: 575.98px)and (orientation:portrait) {
    #nav {
        display: none;
    }
}
@media (min-width: 576px) and (max-width: 991.98px) and (orientation:landscape) {
    #nav {
        display: none;
    }
    .iconDiv{
        margin: 0.2em;
        margin: 10px 10px;
        width: 90px;
        height: 90px;
        border-radius: 50px;
        transition: 1s box-shadow;
    }
    .iconDiv img{
        max-height: 35px;
    }
    #menu {
        display: flex;
        justify-content: center;
        align-content: center;
        position: absolute;
        width: 100px;
        height: 100px;
    } 
}

</style>
