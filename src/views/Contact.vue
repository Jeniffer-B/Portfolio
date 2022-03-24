<template>
    <div class="containerXl bg2">
        <div class="container">
            <div class="informationContainer textStyle1">
                <h3 class="sectionName textColor1">Let's connect!</h3>
                <div class="contactInformation ">
                    <p>e-mail: </p> <p class="email textStyle1 textColor3">jenifferbeltranbarreno@gmail.com</p>
                </div>
                <div class="socialMedia">
                    <p>Social media:</p>
                    <div class="socialIcons">
                        <div>
                            <a href="https://www.linkedin.com/in/jeniffer-beltran-36b22421b/">  
                                <img alt="linkedin" src="@/assets/icons/linkedin.png"> 
                            </a>
                        </div>
                        <div>
                            <a href="https://github.com/Jeniffer-B">
                                <img alt="linkedin" src="@/assets/icons/github.png">
                            </a>
                        </div>
                        <div>
                            <a href="https://www.behance.net/jenifferbeltran">
                                <img alt="behance" src="@/assets/icons/behance.png">
                            </a>
                        </div>
                    </div>
                </div>
            </div>  
            <img class="contactImg" alt="phone" src="@/assets/contact.png"> 
        </div>  
    </div>
</template>
<style scoped>
.contactInformation {
    display: flex;
}
.email {
    border-bottom: #FAB099 3px solid;
}
.socialMedia {
    display: flex;
    flex-direction: column;
}
.socialMedia img {
    width: 50px;
}
.socialIcons {
    display: flex;
}
.socialIcons div {
    margin: 1% 3%;
}
.contactInformation p, .socialMedia p{
    margin:2% 2%;
    font-size: 1.3em;
}

/* tablet */
@media (min-width: 576px) and (max-width: 991.98px) and (orientation:portrait) {
    .informationContainer {
        width: 80%;
    }
    .contactInformation p, .socialMedia p{
    margin:2% 2%;
    font-size: 1.2em;
    }
    .contactImg {
        width: 30%;
    }
}
@media (min-width: 991.98px) and (max-width: 1199.98px)and (orientation:landscape) {
    .informationContainer {
        width: 95%;
    }
    .contactInformation p, .socialMedia p{
        margin:2% 2%;
        font-size: 1.2em;
    }
    .contactImg {
        width: 20%;
    }
}
/*movil*/
@media (max-width: 575.98px)and (orientation:portrait) {
    h3 {    
        font-size: 2.5em;
    }
    .contact {
        flex-direction: column;
    }
    .contactInformation {
        flex-direction: column;
        width: 60%;
    }
    .informationContainer {
        width: 90%;
    }
    .contactInformation p, .socialMedia p{
        margin:1% 1%;
        font-size: 0.8em;
    }
    .contactImg {
        width: 30%;
    }
}
@media (min-width: 576px) and (max-width: 991.98px) and (orientation:landscape) {
    .contact {
        width: 100%;
        justify-content: space-around;
    }
    .informationContainer {
        width: 55%;
    }
    .contactInformation {
        flex-direction: column;
    }
    .email {
        border-bottom: #FAB099 2px solid;
    }
    .contactInformation p, .socialMedia p{
        font-size: 1.2em;
    }
    .contactImg {
        width: 20%;
    }
}
</style>