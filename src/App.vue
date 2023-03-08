<template>
    <nav data-aos="fade-down" class="navbar navbar-expand-lg" id="nav">
  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>
  <div class="collapse navbar-collapse" id="navbarNav">
    <ul class="navbar-nav">
      <li class="nav-item">
        <a class="nav-link active" @click="scroll()">Home</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" @click="scroll2()">About</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" @click="scroll3()">Work</a>
      </li>
    </ul>
  </div>
</nav>
<div data-aos="zoom-in" id="rightLine"><div id="line"></div><a href="mailto:mirzakaric002@gmail.com">mirzakaric002@gmail.com</a></div>
  <div data-aos="zoom-up" id="leftLine"><a href="https://www.linkedin.com/in/mirza-karic-1151811a1/" target="_blank"><img src="./assets/linkedinLogo.png" alt=""></a><div id="line"></div></div>
    <section>
    <div class="container-fluid d-flex align-items-center justify-content-center" id="back1" style="height:100vh;background-color:#0a192f;">
      <div class="container d-flex align-items-center justify-content-around" style="width:1200px">
        <div>
        <h1 data-aos="zoom-in" style="color:white;font-size: 90px;margin: 0;">Mirza Karic</h1>
        <h1 data-aos="zoom-in" style="color:white;font-size: 45px;font-weight:100;"><VueWriter :eraseSpeed="50" :typeSpeed="100" :delay="1000" :array="['Full Stack Developer']"/></h1>

      </div>
      <div>
        <figure data-aos="zoom-in" id="fig">
          <span id="sp"><img id="profile" src="./assets/profilsquare.jpg" alt=""></span>
        </figure>
      </div>
      </div>
    </div>

    <div class="container-fluid d-flex align-items-center justify-content-center back1" id="back2" style="height:100vh;background-color:#0a192f;">
      <div class="container d-flex align-items-center justify-content-around">
        <div id="portfolio">
        <a >About Me</a>
      </div>
      <div id="about">
        <div id="downLeft"></div>
        <p>Hello! My name is Mirza and I enjoy creating things that live on the internet. 
          My interest in web development started back in 2020 and grew since then!
          As a student of Information Technology I am able to work on various projects, in free time I love to learn new technologies!<br>
          With expertise in Front End Development I enjoy other technologies like:<br><br>
          Frontend: Vue.js<br>
          Backend: Django Rest Framework<br>
          Database: MySQL
        </p>
      <div id="upRight"></div>
      </div>
      </div>
    </div>

    <div class="container-fluid d-flex flex-column align-items-center justify-content-center" id="back3" style="height:100vh;background-color:#0a192f;">
      <div id="workHeader">
        <a>Some of My Work</a>
      </div>
      <div class="container d-flex align-items-center justify-content-center">
          <div id="pBoxOne">
            <a href="https://github.com/mirzaak/socialApp" target="_blank"><img src="./assets/socialMedia.png" alt="" ></a>
            <a href="https://github.com/mirzaak/socialApp" target="_blank">Social App</a>
          </div>
          <div id="pBoxTwo">
            <a href="https://github.com/mirzaak/TMDB-MovieApp" target="_blank"><img src="./assets/tmdbhome.png" alt=""></a>
            <a href="https://github.com/mirzaak/TMDB-MovieApp" target="_blank">TMDB Clone App</a>
          </div>
      </div>
    </div>
  </section>
  <router-view/>
</template>
<script setup>


function scroll(){
  var element = document.getElementById("back1");
 element.scrollIntoView();
}
function scroll2(){
  var element = document.getElementById("back2");
 element.scrollIntoView();
}
function scroll3(){
  var element = document.getElementById("back3");
 element.scrollIntoView();
}



</script>
<style>
#nav input{
    margin-left: 20px;
    margin-right: 20px;
    border-radius: 16px;
}
#nav button{
    background: white;
    border-radius: 16px;
}
#nav a{
    padding: 5px;
    color: white;
    font-size: 20px;
    margin: 0 30px 0 30px;
    cursor: pointer;
}
#nav{
    width: 1200px;
    top: 30px;
    position: fixed;
    left: 50%;
    transform: translateX(-50%);
    background: rgba(255, 255, 255, 0.11);
    border-radius: 5px;
    box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
    backdrop-filter: blur(11.6px);
    -webkit-backdrop-filter: blur(11.6px);
}
#navbarNav{
  display: flex;
  align-items: center;
  justify-content: center;
}
::-webkit-scrollbar{
  display: none;
}
section{
  height: 100vh;
  scroll-snap-type: y mandatory;
  overflow-y: auto;
  scroll-behavior: smooth;
  scrollbar-width: none;
}
#back1{
  scroll-snap-align: end;
}
#back2{
  scroll-snap-align: end;
}
#back3{
  scroll-snap-align: end;
}
img{
  width: 300px;
}
#portfolio{
  color: transparent;
  -webkit-text-stroke: 1px white;
  font-size: 80px;
  font-weight: bold;
  position: relative;
  cursor:context-menu;
}
#portfolio::after{
    content: 'About Me';
    position: absolute;
    top: 0;
    left: 0;
    color: #865DFF;
    width: 0;
    overflow: hidden;
    white-space: nowrap;
}
#portfolio:hover::after{
  color: white;
  animation: moveText 0.5s linear both;
}
#workHeader{
  color: transparent;
  -webkit-text-stroke: 1px white;
  font-size: 80px;
  font-weight: bold;
  position: relative;
  cursor:context-menu;
  margin-bottom: 100px;
}
#workHeader::after{
    content: 'Some of My Work';
    position: absolute;
    top: 0;
    left: 0;
    color: #865DFF;
    width: 0;
    overflow: hidden;
    white-space: nowrap;
}
#workHeader:hover::after{
  color: white;
  animation: moveText 0.5s linear both;
}
@keyframes moveText{
    to{
      width:100%;
    }
  }
#fig{
  border: 1px solid white;
}
#sp{
  margin-left: -30px;
  padding-bottom: 30px;
  padding-right: 30px;
  margin-top: -30px;
  width: inherit;
  height: inherit;
  display: block;
}
#rightLine{
  width: 20px;
  height: 20%;
  display: block;
  position: fixed;
  right: 140px;
  top: 0;
  display: flex;
  justify-content: center;
  flex-direction: column;
}
#rightLine a{
  color: white;
  transform-origin: 0 0;
  transform: rotate(90deg);
  margin-left: 23px;
  margin-top: 20px;
  text-decoration: none;
  letter-spacing: 0.5px;
  font-size: 12px;
}
#leftLine{
  width: 20px;
  height: 20%;
  display: block;
  position: fixed;
  left: 140px;
  bottom: 0;
  display: flex;
  align-items: center;
  flex-direction: column;
}
#leftLine img{
  width: 35px;

}
#leftLine a{
  height: 35px;
  margin-bottom: 20px;

}
#line{
    content: "";
    display: block;
    width: 1px;
    height: 100%;
    margin: 0px auto;
    background-color: white;
    bottom: 0;
}
#about{
  width: 600px;
  color: white;
  padding: 30px;
  position: relative;
}
#about p{
  font-size: 20px;
  margin: 0;
}
#downLeft {
  height: 50%; 
  width: 50%;
  position: absolute;
  left: 0;
  bottom: 0; 
  border-left: 1px solid white;
  border-bottom: 1px solid white;
}
#upRight {
  height: 50%; 
  width: 50%;
  position: absolute;
  right: 0;
  top: 0; 
  border-top: 1px solid white;
  border-right: 1px solid white;
}
#pBoxOne{
  margin-right: 50px;
  margin-top: -150px; 
  width: 400px;
  height: 300px;
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;

}
#pBoxOne a{
  font-size: 20px;
  color: white;
  position: absolute;
  opacity: 0.7;
  cursor: pointer;
  text-decoration: none;
}
#pBoxTwo a{
  font-size: 20px;
  color: white;
  position: absolute;
  opacity: 0.7;
  cursor: pointer;
  text-decoration: none;
}
#pBoxOne img:hover{
opacity: 0.3;
}
#pBoxOne img:hover #pBoxOneHover{
opacity: 1;
}
#pBoxTwo img:hover{
opacity: 0.3;
}

#pBoxOne img{
  padding: 10px;
  width: 100%;
  border: 1px solid white;
  opacity: 1;
  transition: 0.5s;
  cursor: pointer;
}
#pBoxTwo{
  width: 400px;
  height: 300px;
  display: flex;
  align-items: center;
  margin-left: 50px;
  justify-content: center;
  position: relative;
}
#pBoxTwo img{
  padding: 10px;
  width: 100%;
  border: 1px solid white;
  opacity: 1;
  transition: 0.5s;
  cursor: pointer;
}

</style>
