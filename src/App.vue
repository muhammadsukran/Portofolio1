<template>
  <div class="app">
    <!-- Pemanggilan Komponen Background -->
    <Background />
    
    <div class="hedder">
      
      <h1 :class="{ 'animate__animated animate__slideInDown': shouldAnimate }">My abilities and mastery of skills</h1>
    </div>

    <div class="navigation">
      <Navigation />
    </div>
    <!-- Konten lainnya -->
    <div class="content">
      <!-- Pemanggilan Komponen SVG -->
      <SvgComponent />
      
      <!-- Pemanggilan Komponen Profile -->
      <Profile />
      <h2>Muhammad Sukran</h2>
      
      <!-- Pemanggilan Komponen Icon -->
      
    </div>
    <div class="icon-container">
      <Icon /> 
      
    </div>

    <div class="svg-contain">
      <cv />
    </div> 

    <div class="Ahli-contain">
      <Ahli />
    </div> 
    <div class="button">
      <animatedbutton />
    </div>

    <div class="pointer">
      <pointer />
    </div>
  </div>
</template>

<script>
import cv from './components/icons/IconCommunity.vue';
import Icon from './components/icons/Icon.vue';
import Ahli from './components/icons/IconDocumentation.vue'
import SvgComponent from './components/SvgComponent.vue';
import Profile from './components/Profile.vue';
import Background from './components/frost.vue'; 
import pointer from './components/pointer.vue'; 
import animatedbutton from './components/HelloWorld.vue';
import Navigation from './components/WelcomeItem.vue';

export default {
  name: 'App',
  components: {
    Icon ,
    SvgComponent,
    Profile,
    Background,
    cv,
    Ahli,
    animatedbutton,
    Navigation,
    pointer
  },
  data() {
    return {
      shouldAnimate: true // Menambahkan properti shouldAnimate
    };
  },
  mounted() {
    // Set shouldAnimate menjadi true saat komponen dimount
    this.shouldAnimate = true;
  }
}
</script>

<style>
@import url('https://fonts.cdnfonts.com/css/jorgey');
@import url('https://fonts.cdnfonts.com/css/rem');
h1{
  width: 500px; 
  display: flex;
  position: fixed;
  justify-content: center;
  align-items: center;
  font-family: 'Jorgey', sans-serif;                                            
  fill: wheat;
  z-index: 3;
  text-shadow: transparent;
  margin-top: -300px;
  margin-left: -150px; 
  width: 100%;
  animation: shadow 3s infinite alternate;
}
@keyframes shadow {
  0% {
    text-shadow: 0 0 10px #000; /* Bayangan awal */
  }
  50% {
    text-shadow: 0 0 10px #00f; /* Bayangan di tengah animasi */
  }
  100% {
    text-shadow: 0 0 10px #0f0; /* Bayangan akhir */
  }
}
.button {
  z-index: 4;
  position: fixed;
  top: 80%;
  left: 50%;
  transform: translate(-50%, -50%);
  align-items: center;
  justify-content: center;
}

.navigation{
  text-align: center;
  position: fixed;
  z-index: 4;
}

h2{
  margin-left: -100px;
  margin-top: -180px;
  position: fixed;
  font-family: 'REM', sans-serif;

}


.app {
  position: relative; 
  z-index: 1; 
}

.content {
  position: relative; 
  z-index: 2; 
}

.Ahli-contain {
   width: 500px; 
  display: flex;
  position: fixed;
  justify-content: center;
  align-items: center;
  fill: ghostwhite;
  z-index: 3;
  margin-top: -140px;
  margin-left: -260px;
}
.Ahli-contain > * {
  margin-left: 10px; 
  width: 30px; 
  height: auto; 
  filter: drop-shadow(0 0 10px #000035);
}
.icon-container {
  display: flex;
  align-items: center; 
  justify-content: center; 
  position: fixed;
  bottom: 0;
  right: 0;
  top: -600px;
  padding: 0 100px;
  z-index: 3;
}

.icon-container > * {
  margin-left: 10px; 
  width: 30px; 
  height: auto; 
  filter: drop-shadow(0 0 10px #000035);
}
.icon-container:hover{
  background-color: transparent;
  filter: drop-shadow(0px 0px 30px #88c6f2);
}

.svg-contain {
  width: 500px; 
  display: flex;
  position: fixed;
  justify-content: center;
  align-items: center;
  fill: wheat;
  z-index: 3;
  margin-top: -200px;
  margin-left: 350px;
  
}
.svg-contain > *{
  margin-right: 10px;
  margin-left: 30px;

}
</style>
