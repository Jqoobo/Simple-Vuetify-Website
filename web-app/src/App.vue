<template>
  <v-app>
    <Header/>
    <v-main>
      <HeroComponent/>
      <Onas/>
      <Portfolio/>
      <Gallery/>
      <Weather/>
      <Contact/>   
      <Footer/>
    </v-main>
  </v-app>
</template>

<script>

import HeroComponent from './components/HeroComponent.vue';
import Contact from './components/Contact.vue';
import Footer from './components/Footer.vue';
import Header from './components/header.vue';
import Weather from './components/Weather.vue';
import Portfolio from './components/Portfolio.vue';
import Gallery from './components/Gallery.vue';
import Onas from './components/Onas.vue';


export default {
  name: 'App',
  components: { HeroComponent, Contact, Footer, Header, Weather, Portfolio, Gallery, Onas },
  
};
</script>
