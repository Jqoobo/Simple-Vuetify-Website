<template>
  <v-container class="my-15">
    <v-row justify="center">
        <v-col lg="12" class="text-center">
            <v-subheader class="text-h4 justify-center black--text mb-5">Polecane Hotele</v-subheader>
            <p class="black--text">Hotele w których będziesz czuć się jak w domu!</p>
        </v-col>

  <v-col lg="4">
        <v-card
    class="mx-auto my-12"
    max-width="374"
  >
    <v-img
      height="250"
      src="https://media.hrs.com/media/image/11/82/8c/InterContinental_Hotels_WARSAW-Warschau-Aussenansicht-9-153036.jpg"
    ></v-img>

    <v-card-title class="justify-center">InterContinental Warszawa</v-card-title>

    <v-card-text>
     
      <div class="black--text text-justify">Ekskluzywny hotel konferencyjny usytuowany w wieżowcu położonym przy Pałacu Kultury i Nauki oraz parku Świętokrzyskim.</div>
    </v-card-text>

    <v-divider class="mx-4"></v-divider>
    <v-card>
        <v-card-actions>
            <v-btn color="teal lighten-1 white--text" rounded href="https://warszawa.intercontinental.com/">Sprawdź hotel</v-btn>
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

  <v-col lg="4">
        <v-card
    class="mx-auto my-12"
    max-width="374"
  >
    <v-img
      height="250"
      src="https://rzeszow-news.pl/wp-content/uploads/2017/03/Hotel-Bristol-.jpg"
    ></v-img>

    <v-card-title class="justify-center">Hotel Bristol Rzeszów</v-card-title>

    <v-card-text>
     
      <div class="black--text text-justify">Spokojny hotel z restauracją i japońską knajpką, kameralnym barem i bezpłatnym dostępem do sieci Wi-Fi.</div>
    </v-card-text>

    <v-divider class="mx-4"></v-divider>
    <v-card>
        <v-card-actions>
            <v-btn color="teal lighten-1 white--text" rounded href="https://www.bristol-rzeszow.pl/">Sprawdź hotel</v-btn>
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

  <v-col lg="4">
        <v-card
    class="mx-auto my-12"
    max-width="374"
  >
    <v-img
      height="250"
      src="https://cf.bstatic.com/xdata/images/hotel/max1024x768/216242641.jpg?k=54b39b89388afb0626eb539cdb2c243f3a2194fcb96102fbe26a17eb5a2b0522&o=&hp=1"
    ></v-img>

    <v-card-title class="justify-center">Novotel Kraków</v-card-title>

    <v-card-text>
     
      <div class="black--text text-justify">Eleganckie pokoje i apartamenty, niektóre z widokiem na zamek, przestronna restauracja, basen kryty i sauna.</div>
    </v-card-text>

    <v-divider class="mx-4"></v-divider>
    <v-card>
        <v-card-actions>
            <v-btn color="teal lighten-1 white--text" rounded href="https://all.accor.com/hotel/3372/index.pl.shtml?utm_campaign=seo+maps&utm_medium=seo+maps&utm_source=google+Maps">Sprawdź hotel</v-btn>
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

<style scoped></style>