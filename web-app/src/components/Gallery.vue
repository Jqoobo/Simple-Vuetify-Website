<template>
  <v-container class="my-15">
    <v-row justify="center">
        <v-col lg="12" class="text-center ">
            <v-subheader class="text-h4 justify-center d-none d-sm-flex ">Galeria</v-subheader>
            <p class=" justify-center d-none d-sm-flex">Trochę piekna z pozostałych częsci Naszego pięknego kraju!</p>
            <v-subheader class="text-h4 justify-center d-flex d-sm-none">Galeria</v-subheader>
            <p class="text-center d-flex d-sm-none">Trochę piekna z pozostałych częsci Naszego pięknego kraju!</p>
        </v-col>     
        
    <v-col
      class="d-none d-sm-flex "
      cols="9"
    >
      <v-img
        :src="'https://i.wpimg.pl/1200x/d.wpimg.pl/576964982-998273013/gory-aktywnie-weekend.jpg'"
        aspect-ratio="1"
        class="grey lighten-2 ml-10"
      >
        <template v-slot:placeholder>
          <v-row
            class="fill-height ma-0"
            align="center"
            justify="center"
          >
            <v-progress-circular
              indeterminate
              color="grey lighten-5"
            ></v-progress-circular>
          </v-row>
        </template>
      </v-img>
       <v-img
        :src="'https://doba.pl/media/powiaty/wroclaw/articles/images/22342/doba_pl_68666-0d19c68577d38e93fadbf0996f6d1004_1280x720.jpg'"
        aspect-ratio="1"
        class="grey lighten-2 ml-10"
      >
        <template v-slot:placeholder>
          <v-row
            class="fill-height ma-0"
            align="center"
            justify="center"
          >
            <v-progress-circular
              indeterminate
              color="grey lighten-5"
            ></v-progress-circular>
          </v-row>
        </template>
      </v-img>
       <v-img
        :src="'https://polskazachwyca.pl/wp-content/uploads/2017/11/moszna-shutterstock_45201820-e1511825136853.jpg'"
        aspect-ratio="1"
        class="grey lighten-2 ml-10"
      >
        <template v-slot:placeholder>
          <v-row
            class="fill-height ma-0"
            align="center"
            justify="center"
          >
            <v-progress-circular
              indeterminate
              color="grey lighten-5"
            ></v-progress-circular>
          </v-row>
        </template>
      </v-img>
    </v-col>



    <v-col
      class="d-flex d-sm-none"
      cols="12"
    >
      <v-img
        :src="'https://i.wpimg.pl/1200x/d.wpimg.pl/576964982-998273013/gory-aktywnie-weekend.jpg'"
        aspect-ratio="1"
        class="grey lighten-2"
      >
        <template v-slot:placeholder>
          <v-row
            class="fill-height ma-0"
            align="center"
            justify="center"
          >
            <v-progress-circular
              indeterminate
              color="grey lighten-5"
            ></v-progress-circular>
          </v-row>
        </template>
      </v-img>

      <v-img
        :src="'https://doba.pl/media/powiaty/wroclaw/articles/images/22342/doba_pl_68666-0d19c68577d38e93fadbf0996f6d1004_1280x720.jpg'"
        aspect-ratio="1"
        class="grey lighten-2"
      >
        <template v-slot:placeholder>
          <v-row
            class="fill-height ma-0"
            align="center"
            justify="center"
          >
            <v-progress-circular
              indeterminate
              color="grey lighten-5"
            ></v-progress-circular>
          </v-row>
        </template>
      </v-img>

      <v-img
        :src="'https://polskazachwyca.pl/wp-content/uploads/2017/11/moszna-shutterstock_45201820-e1511825136853.jpg'"
        aspect-ratio="1"
        class="grey lighten-2"
      >
        <template v-slot:placeholder>
          <v-row
            class="fill-height ma-0"
            align="center"
            justify="center"
          >
            <v-progress-circular
              indeterminate
              color="grey lighten-5"
            ></v-progress-circular>
          </v-row>
        </template>
      </v-img>
    </v-col>

        </v-row>
        </v-container>
</template>

<script>
export default {
       name: "Gal-erry"
}
</script>

<style scoped>


</style>