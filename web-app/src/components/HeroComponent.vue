<template>
    <v-container>
        <v-row>
            <v-col lg="6">
               <h2 class="intro-text">Witamy na naszej stronie!</h2>
               <p class="opis">V</p>
               <v-btn color="cyan" class="white--text" rounded>Zacznij</v-btn>
               <v-btn color="success" class="white--text" rounded>
               <v-icon>mdi-play-circle</v-icon>Zobacz wideo
               </v-btn>
            </v-col>
            <v-col lg="6">
                <img width="100%" src="./../assets/car.jpg"/>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
export default{ 
    name: "HeroComponent"
 }

</script>

<style scoped>

h2.intro-text{
    font-size:60px;
    font-weight: bold;
    font-family: cursive;
    color:#444
}

</style>
