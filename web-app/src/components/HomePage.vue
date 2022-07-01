<template>
    <v-container class="pt-15">
        <v-row>
            <img class="hero d-flex d-sm-none ml-5" src="https://a.allegroimg.com/original/116527/c2a389954a7c8524835cad1eb9ab%22/%3E"/>
            <v-col lg="6">
               <h2 class="intro-text text-left d-none d-sm-flex">Poznaj Polskę!</h2>
               <h2 class="intro-text text-center ml-15 pl-5 d-flex d-sm-none">Poznaj Polskę!</h2> <br><br>
               <p class="opis d-none d-sm-flex d-sm-none d-md-flex black--text">Nasza strona przedstawia najlepsze zakątki Polski oraz całe piekno naszego kraju! Odkryj cuda tego kraju już teraz!<br><br>Polska, oficjalnie Rzeczpospolita Polska, jest demokratycznym państwem w Europie Środkowej. Stolicą i największym miastem kraju jest Warszawa. Polska, z powierzchnią 312 696 km² jest dziewiątym, co do wielkości krajem w Europie i zajmuje 69 miejsce wśród największych państw świata. Od północy Polska graniczy z Rosją i Litwą, od wschodu z Białorusią i Ukrainą, od południa ze Słowacją i Czechami, od zachodu z Niemcami. Geograficznie Polska jest krajem nizinnym. Katolicy są zdecydowanie największą religią w kraju.</p>
               <p class="justify-center text-justify d-flex d-sm-none black--text">Nasza strona przedstawia najlepsze zakątki Polski oraz całe piekno naszego kraju! Odkryj cuda tego kraju już teraz!<br><br>Polska, oficjalnie Rzeczpospolita Polska, jest demokratycznym państwem w Europie Środkowej. Stolicą i największym miastem kraju jest Warszawa. Polska, z powierzchnią 312 696 km² jest dziewiątym, co do wielkości krajem w Europie i zajmuje 69 miejsce wśród największych państw świata. Od północy Polska graniczy z Rosją i Litwą, od wschodu z Białorusią i Ukrainą, od południa ze Słowacją i Czechami, od zachodu z Niemcami. Geograficznie Polska jest krajem nizinnym. Katolicy są zdecydowanie największą religią w kraju.</p>
               <v-btn color="teal lighten-1" class="white--text mr-10 mt-10 ml-5 " href="#/portfolio" rounded>Zacznij</v-btn>
               <v-btn color="teal darken-3" class="white--text mt-10 ml-5" rounded href="https://www.youtube.com/watch?v=ekz6i58kVpI">
               <v-icon class="mr-3">mdi-play-circle</v-icon>Zobacz wideo
               </v-btn>
            </v-col>
            <v-col lg="6" class="d-none d-sm-flex">
                <img class="hero d-none d-sm-flex" src="https://a.allegroimg.com/original/116527/c2a389954a7c8524835cad1eb9ab%22/%3E"/>
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
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    text-align: center;
    margin-right: 25%;
    color:#444
}

p.opis{
    font-size: 16px;
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    text-align: justify;
    margin: 32 px 0px;
    margin-right: 25%;
    color: #444444ba;
}


.hero{
height: 90%;
    width:90%
}

.hero2{
    height: 65%;
    width:65%
}

</style>
 