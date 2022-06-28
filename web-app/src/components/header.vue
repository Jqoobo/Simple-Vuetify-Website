<template>
  <v-app>
    <v-app-bar 
      style="padding: 0px 90px"
      app
      color="white"
      light
      elevation="6"
      elevate-on-scroll
    >
    <v-toolbar-title>
      Vuetify APP
    </v-toolbar-title>
    <v-spacer/>
    <v-list class="d-flex align-center">
      <v-list-item link v-for="(menu,index) in menus" :key="index" :to="menu.route">
        <v-list-title>{{menu.title}}</v-list-title>
      </v-list-item>
      <v-btn text > 
        <v-icon>mdi-magnify</v-icon>
      </v-btn>
      <v-btn outlined color="cyan">Zacznij</v-btn>
      </v-list>
    </v-app-bar>


    

    <v-main>
      
    </v-main>
  </v-app>
</template>

<script>


export default {
  name: "Header-page",
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
