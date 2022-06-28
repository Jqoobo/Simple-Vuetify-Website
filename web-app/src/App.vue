<template>
  <v-app>
    <Header/>
    <v-main>
      <HeroComponent/>
    </v-main>
  </v-app>
</template>

<script>

import Header from './components/header.vue';
import HeroComponent from './components/HeroComponent.vue';
export default {
  name: 'App',
  components: { HeroComponent, Header},
  data(){
   return{
    menus:[
      {title:'Strona Główna',   route:'glowna'},
      {title:'O nas',           route:'o-nas'},
      {title:'Portfolio',       route:'portfolio'},
      {title:'Projekty',        route:'projekt'},
      {title:'Galeria',         route:'galeria'},
      {title:'Kontakt',         route:'kontakt'},
    ]
   }
  }
  

  
};
</script>
