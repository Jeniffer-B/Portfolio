<template>
  <div class="about">
    <div class="aboutMe">
      Lorem ipsum dolor, sit amet consectetur adipisicing elit. 
      Sint harum rem asperiores cupiditate aliquam fuga provident sit alias impedit, 
      magni facilis inventore deserunt eos libero enim laudantium autem iste. Porro?
      Lorem ipsum dolor, sit amet consectetur adipisicing elit. 
      <br>
      Sint harum rem asperiores cupiditate aliquam fuga provident sit alias impedit, 
      magni facilis inventore deserunt eos libero enim laudantium autem iste. Porro?
    </div>
      <img class="aboutImg" src="@/assets/aboutMe.png" alt="ilustration"> 
  </div>
</template>
<style scoped>
.about {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  align-items: center;
  height: 100vh;
  background-color: #B97CA2;
}
.aboutMe {
  width: 35%;
  height: auto;
  text-align: left;
  font-family: 'Roboto Serif', sans-serif;
  letter-spacing: 0.2em;
  line-height: 2em;
  font-size: 1.2em;
  color: #fff;
}
.aboutImg {
  width: 30%;
}
/* tablet */
@media (min-width: 576px) and (max-width: 991.98px) and (orientation:portrait) {
  .aboutMe {
    width: 90%;
  }
  .aboutImg {
    width: 50%;
  }
}
@media (min-width: 991.98px) and (max-width: 1199.98px)and (orientation:landscape) {
  .aboutMe {
    width: 40%;
    line-height: 1.5em;
    font-size: 1em;
  }
  .aboutImg {
    width: 30%;
  }
}
/*movil*/
@media (max-width: 575.98px)and (orientation:portrait) {
  .aboutMe {
    width: 90%;
    height: auto;
    text-align: left;
    letter-spacing: 0.2em;
    line-height: 1.3em;
    font-size: 0.9em;
 } 
  .aboutImg {
    width: 70%;
  }
}
@media (min-width: 576px) and (max-width: 991.98px) and (orientation:landscape) {
  .aboutMe {
    width: 80%;
    height: auto;
    text-align: left;
    letter-spacing: 0.2em;
    line-height: 1em;
    font-size: 0.9em;
    margin: 2%;
 } 
  .aboutImg {
    width: 20%;
  }
}
</style>
