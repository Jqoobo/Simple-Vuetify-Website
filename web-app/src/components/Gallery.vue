<template>
  <v-container class="my-15">
    <v-row justify="center">
        <v-col lg="12" class="text-center ">
            <v-subheader class="text-h4 justify-center d-none d-sm-flex ">Gallery</v-subheader>
            <p class=" justify-center d-none d-sm-flex">Lorem ipsum Lorem ipsum Lorem ipsum Lorem ipsum</p>
            <v-subheader class="text-h4 justify-center d-flex d-sm-none">Gallery</v-subheader>
            <p class="text-center d-flex d-sm-none">Lorem ipsum Lorem ipsum Lorem ipsum Lorem ipsum</p>
        </v-col>     
        
    <v-col
      v-for="n in 9"
      :key="n"
      class="d-none d-sm-flex "
      cols="3"
    >
      <v-img
        :src="`https://picsum.photos/500/300?image=${n * 5 + 10}`"
        :lazy-src="`https://picsum.photos/10/6?image=${n * 5 + 10}`"
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

    <v-col
      v-for="n in 9"
      :key="n"
      class="d-flex d-sm-none"
      cols="8"
    >
      <v-img
        :src="`https://picsum.photos/500/300?image=${n * 5 + 10}`"
        :lazy-src="`https://picsum.photos/10/6?image=${n * 5 + 10}`"
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