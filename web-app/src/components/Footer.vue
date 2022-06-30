<template>
  <v-footer padless>
    <v-col lg="12">
        <v-row justify="center">
           <v-col lg="4" class="text-center">
            <v-toolbar-title class="logo_title">ODKRYWAJ.pl</v-toolbar-title>
            <v-card-text class="">
        <v-row justify="center" class="ml-3 mt-2">
          <h3 class="h3_profile">Kuba</h3>
        <v-btn
          class="mx-4 black--text"
          icon
          href="https://www.linkedin.com/in/jakub-rzepka/"
        >
          <v-icon size="24px">
            mdi-linkedin  
          </v-icon>
        </v-btn>
        </v-row>
        <v-row justify="center" class="ml-3">
          <h3 class="h3_profile">Kamila</h3>
        <v-btn
          class="mx-4 black--text"
          icon
          href="https://www.linkedin.com/in/kamila-talaj"
        >
          <v-icon size="24px">
            mdi-linkedin
          </v-icon>
        </v-btn>
        </v-row>
      </v-card-text>
      <v-subheader class="mt-3 justify-center black--text">Zapisz się do Newsletter'a już teraz!</v-subheader>
      <v-form class="mt-4">
        <v-text-field label="Wpisz Email" outlined dense required />
        <v-btn rounded class="white--text"  color="teal lighten-1">Zasubskrybuj</v-btn>
      </v-form>
           </v-col>
           
        </v-row>
        <div class="mt-10">
            <v-divider></v-divider>
            <v-subheader>
                Strona stworzona przy pomocy Vue oraz Vuetify
            <v-spacer />
            <strong class="d-none d-sm-flex">Designed by Kuba & Kamila</strong>
            </v-subheader>
           </div>
    </v-col>
  </v-footer>
</template>

<script>
export default {
   name:"foo-ter",
}
</script>

<style scoped>
.h3_profile{
  padding-top:7px;
}

@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@500&display=swap');
.logo_title{
font-family: 'Segoe UI';
font-weight: 800;
 }

</style>