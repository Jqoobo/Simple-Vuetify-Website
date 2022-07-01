<template>
  <v-container class="my-15">
    <v-row justify="center">
        <v-col lg="12" class="text-center">
            <v-subheader class="text-h4 justify-center d-none d-sm-flex black--text">Galeria</v-subheader><br>
            <p class=" justify-center d-none d-sm-flex black--text">Trochę piękna z pozostałych częsci naszego pięknego kraju!</p>
            <v-subheader class="text-h4 justify-center d-flex d-sm-none black--text" style="margin-top:-50px">Galeria</v-subheader><br>
            <p class="text-center d-flex d-sm-none black--text">Trochę piękna z pozostałych części naszego pięknego kraju!</p>
        </v-col>

         <!--Responsywność - Desktop-->
        <v-row class="mx-5 mt-10 ml-15 justify-center d-none d-sm-flex ">
    <v-col
      cols="6"
      sm="4"
    >
      <v-img
        src="https://i.wpimg.pl/1200x/d.wpimg.pl/576964982-998273013/gory-aktywnie-weekend.jpg"
        style="width: 500px; height:300px;"
        class="ml-3 d-none d-sm-flex "
      ></v-img>
    </v-col>

    <v-col
      cols="6"
      sm="4"
    >
      <v-img src="https://doba.pl/media/powiaty/wroclaw/articles/images/22342/doba_pl_68666-0d19c68577d38e93fadbf0996f6d1004_1280x720.jpg"
      style="width: 500px; height:300px;"
      class="d-none d-sm-flex"
      ></v-img>
    </v-col>

    <v-col
      cols="6"
      sm="4"
    >
      <v-img src="https://polskazachwyca.pl/wp-content/uploads/2017/11/moszna-shutterstock_45201820-e1511825136853.jpg"
      style="width: 500px; height:300px; margin-left:-15px"
      class="d-none d-sm-flex"
      ></v-img>
    </v-col>
    <v-col
      cols="6"
      sm="4"
    >
      <v-img src="https://i.gremicdn.pl/image/free/8a26580a4c0d813ce2994667d6ad8832/?t=resize:fill:1200:716,enlarge:1"
      style="width: 500px; height:300px;"
      class="d-none d-sm-flex"
      ></v-img>
    </v-col>
  </v-row>
     
    <!--Responsywność - Mobile-->
    <v-row class="mx-5 justify-center d-flex d-sm-none">
    <v-col
      cols="6"
      sm="4"
    >
      <v-img
        src="https://i.wpimg.pl/1200x/d.wpimg.pl/576964982-998273013/gory-aktywnie-weekend.jpg"
        style="width: 300px; height:150px;"
        class="ml-3 d-flex d-sm-none"
      ></v-img>
    </v-col>

    <v-col
      cols="6"
      sm="4"
    >
      <v-img src="https://doba.pl/media/powiaty/wroclaw/articles/images/22342/doba_pl_68666-0d19c68577d38e93fadbf0996f6d1004_1280x720.jpg"
      style="width: 300px; height:150px;"
      class="d-flex d-sm-none"
      ></v-img>
    </v-col>

    <v-col
      cols="6"
      sm="4"
    >
      <v-img src="https://polskazachwyca.pl/wp-content/uploads/2017/11/moszna-shutterstock_45201820-e1511825136853.jpg"
      style="width: 300px; height:150px;"
      class="ml-3 d-flex d-sm-none"
      ></v-img>
    </v-col>
    <v-col
      cols="6"
      sm="4"
    >
      <v-img src="https://i.gremicdn.pl/image/free/8a26580a4c0d813ce2994667d6ad8832/?t=resize:fill:1200:716,enlarge:1"
      style="width: 300px; height:150px;"
      class="d-flex d-sm-none"
      ></v-img>
    </v-col>
  </v-row>

</v-row>
</v-container>
</template>

<script>
export default {
       name: "Gal-erry"
}
</script>

<style scoped></style>