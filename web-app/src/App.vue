<template>
  <v-app>
    <Header/>
    <v-main>
      <HeroComponent/>
      <onas/>
      <Portfolio/>
      <project/>
      <Gallery/>
      <Contact/>
      <Footer/>
    </v-main>
  </v-app>
</template>

<script>

import HeroComponent from './components/HeroComponent.vue';
import Onas from './components/Onas.vue';
import Portfolio from './components/Portfolio.vue';
import Project from './components/Project.vue';
import Gallery from './components/Gallery.vue';
import Contact from './components/Contact.vue';
import Footer from './components/Footer.vue';
import Header from './components/header.vue';

export default {
  name: 'App',
  components: { HeroComponent, Onas, Portfolio, Project, Gallery, Contact, Footer, Header },
  
};
</script>
