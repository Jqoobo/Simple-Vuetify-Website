<template>
  <v-footer padless>
    <v-col lg="12">
        <v-row justify="center">
           <v-col lg="4" class="text-center">
            <v-toolbar-title>Vuetify App</v-toolbar-title>
            <v-card-text>
        <v-btn
          v-for="icon in icons"
          :key="icon"
          class="mx-4 black--text"
          icon
        >
          <v-icon size="24px">
            {{ icon }}
          </v-icon>
        </v-btn>
      </v-card-text>
      <v-subheader>Lorem ipsum Lorem ipsum Lorem ipsum Lorem ipsum</v-subheader>
      <v-form class="mt-4">
        <v-text-field label="Email" outlined dense />
        <v-btn rounded color="cyan">Subscribe us</v-btn>
      </v-form>
           </v-col>
           
        </v-row>
        <div class="mt-10">
            <v-divider></v-divider>
            <v-subheader>
                Copyright Vuetify App. All Rights Reserverd {{ new Date().getFullYear() }} — <strong>Vuetify</strong> 
            <v-spacer />
            <strong>Designed by Kuba & Kamila</strong>
            </v-subheader>
           </div>
    </v-col>
  </v-footer>
</template>

<script>
export default {
   name:"foo-ter",
   data(){
    return{
        icons: [
        'mdi-facebook',
        'mdi-twitter',
        'mdi-linkedin',
        'mdi-instagram',
      ],
      }
   }
}
</script>

<style scoped>


</style>