<template>
  <v-app>
    <v-app-bar 
      style="padding: 0px 90px"
      app
      color="white"
      light
      elevation="6"
      elevate-on-scroll
      class="d-flex justify-center"
    >
    <img class="img d-none d-sm-flex"  src="https://media.discordapp.net/attachments/808637296286892082/992003976872607845/logo_black.png?width=905&height=905"/>
    <v-toolbar-title  class="logo_title mx-2 d-none d-sm-flex">ODKRYWAJ.pl </v-toolbar-title>
    <img class="img2 d-flex d-sm-none"  src="https://media.discordapp.net/attachments/808637296286892082/992003976872607845/logo_black.png?width=905&height=905"/>
    <v-toolbar-title class="mx-2 mr-15 pr-15 d-flex d-sm-none">Odrywaj.pl</v-toolbar-title>
    <v-spacer/>
    <v-list class="align-center d-none d-sm-flex d-sm-none d-md-flex">
         <v-btn outlined color="black" class="mx-2" href="#/home">Home</v-btn>
         <v-btn outlined color="black" class="mx-2" href="#/onas">O nas</v-btn>
         <v-btn outlined color="black" class="mx-2" href="#/portfolio">Portfolio</v-btn>
         <v-btn outlined color="black" class="mx-2" href="#/gallery">Galeria</v-btn>
         <v-btn outlined color="black" class="mx-2" href="#/weather">Pogoda</v-btn>
      </v-list>
      <div class="hidden-sm-and-up">
        <v-menu offset-y>
      <template v-slot:activator="{ on }">
        <v-btn
          color="teal lighten-1"
          dark
          v-on="on"
        >
          Rozwiń
        </v-btn>
      </template>
      <v-list class="rensponsivMenu">
        <v-list-item>
          <v-list-item-title><v-btn outlined color="black" class="mx-2" href="#/home">Home</v-btn></v-list-item-title>
          </v-list-item>
          <v-list-item>
          <v-list-item-title><v-btn outlined color="black" class="mx-2" href="#/onas">O nas</v-btn></v-list-item-title>
          </v-list-item>
          <v-list-item>
          <v-list-item-title><v-btn outlined color="black" class="mx-2" href="#/portfolio">Portfolio</v-btn></v-list-item-title>
          </v-list-item>
          <v-list-item>
          <v-list-item-title><v-btn outlined color="black" class="mx-2" href="#/gallery">Galeria</v-btn></v-list-item-title>
          </v-list-item>
          <v-list-item>
          <v-list-item-title><v-btn outlined color="black" class="mx-2" href="#/weather">Pogoda</v-btn></v-list-item-title>
        </v-list-item>
      </v-list>
    </v-menu>
      </div>
    </v-app-bar>
    <v-main>
      <component :is="currentView" />
      <Contact/>
      <Footer/>
    </v-main>
  </v-app>
</template>

<script>

import HeroComponent from './components/HeroComponent.vue'
import Contact from './components/Contact.vue'
import Footer from './components/Footer.vue'
import Header from './components/header.vue'
import Weather from './components/Weather.vue'
import Portfolio from './components/Portfolio.vue'
import Gallery from './components/Gallery.vue'
import Onas from './components/Onas.vue'


const routes = {
  '/home': HeroComponent,
  '/onas': Onas,
  '/portfolio': Portfolio,
  '/gallery': Gallery,
  '/weather': Weather
}


export default {
  name: 'App',
  components: { HeroComponent, Contact, Footer, Header, Weather, Portfolio, Gallery, Onas },
  
  data() {
    return {
      currentPath: window.location.hash
    }
  },
  computed: {
    currentView() {
      return routes[this.currentPath.slice(1) || '/']
    }
  },
  mounted() {
    window.addEventListener('hashchange', () => {
		this.currentPath = window.location.hash
		})
  }
};
</script>

<style scoped>
.img{
width: 3%;
font-family: "";
}

.img2{
  width: 12%;
  }
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@500&display=swap');
  .logo_title
 {
font-family: 'Segoe UI';
font-weight: 800;
 }

</style>