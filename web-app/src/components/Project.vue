<template>
  <v-container class="my-15">
    <v-row justify="center">
        <v-col lg="12" class="text-center">
            <v-subheader class="text-h4 justify-center">Project</v-subheader>
            <p>Lorem ipsum Lorem ipsum Lorem ipsum Lorem ipsum</p>
        </v-col>

        <v-col lg="4" v-for="project in 3" :key="project">
        <v-card
    class="mx-auto my-12"
    max-width="374"
  >
    <v-img
      height="250"
      src="./../assets/car.jpg"
    ></v-img>

    <v-card-title>Web Dev</v-card-title>

    <v-card-text>
     
      <div>Small plates, salads & sandwiches - an intimate setting with 12 indoor seats plus patio seating.</div>
    </v-card-text>

    <v-divider class="mx-4"></v-divider>
    <v-card>
        <v-card-actions>
            <v-btn color="cyan" rounded>View Details</v-btn>
            <v-spacer/>
            <v-rating
            :value="4.5"
            color="amber"
            dense
            half-increments
            readonly
            size="14"
            >
            </v-rating>
            </v-card-actions>
    </v-card>
    

  </v-card>
  </v-col>
    </v-row>
    </v-container>
</template>

<script>
export default {
        name: "Pro-ject"
}
</script>

<style  scoped>

</style>