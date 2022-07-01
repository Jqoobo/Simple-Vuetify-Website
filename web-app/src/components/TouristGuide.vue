<template>
<v-container class="my-15">
    <v-row justify="center">
        <v-col lg="12" class="text-center">
            <v-subheader class="text-h4 justify-center 	d-none d-sm-flex black--text">Najpiękniejsze Polskie Miasta</v-subheader>
            <v-subheader class="text-h4 justify-center 	d-flex d-sm-none black--text mb-4">Najpiękniejsze Polskie Miasta</v-subheader><br>
            <p class="black--text">W tym miejscu możesz doświadczyć najpiekniejszych widoków Polski przed swoim ekranem!</p>
        </v-col>
        <v-col lg="12">
            <div class="justify-center mt-5 mb-10 d-none d-sm-flex ">
                <v-chip @click="activePortfolio = 'webapp'" :color="activePortfolio === 'webapp'? 'teal lighten-1':''" class="mx-5 font-weight-bold ">Warszawa</v-chip>
                <v-chip @click="activePortfolio = 'mobileapp'" :color="activePortfolio === 'mobileapp'? 'teal lighten-1':''" class="mx-5 font-weight-bold">Rzeszów</v-chip>
                <v-chip @click="activePortfolio = 'desktopapp'" :color="activePortfolio === 'desktopapp'? 'teal lighten-1':''" class="mx-5 font-weight-bold">Kraków</v-chip>
            </div>
            <div class="justify-center mt-5 mb-8 d-flex d-sm-none">
                <v-chip @click="activePortfolio = 'webapp'" :color="activePortfolio === 'webapp'? 'teal lighten-1':''" class="mx-5 font-weight-bold ">Warszawa</v-chip>
                <v-chip @click="activePortfolio = 'mobileapp'" :color="activePortfolio === 'mobileapp'? 'teal lighten-1':''" class="mx-5 font-weight-bold">Rzeszów</v-chip>
                <v-chip @click="activePortfolio = 'desktopapp'" :color="activePortfolio === 'desktopapp'? 'teal lighten-1':''" class="mx-5 font-weight-bold">Kraków</v-chip>
            </div>
        </v-col>
        <slot v-if="activePortfolio === 'webapp'">
        <v-col lg="3" v-for="(web,webindex) in webApps" :key="webindex">
            <v-card>
                <v-img
                :src="web.image"
                class="white--text align-end"
                gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                height="200px"
                >
                <v-card-title>{{web.title}}</v-card-title>
                </v-img>
            </v-card>
        </v-col>
        </slot>
        <slot v-if="activePortfolio === 'mobileapp'">
        <v-col lg="3" v-for="(mobile,mobileindex) in mobileApps" :key="mobileindex">
            <v-card>
                <v-img
                :src="mobile.image"
                class="white--text align-end"
                gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                height="200px"
                >
                <v-card-title>{{mobile.title}}</v-card-title>
                </v-img>
            </v-card>
        </v-col>
        </slot>
        <slot v-if="activePortfolio === 'desktopapp'">
        <v-col lg="3" v-for="(desktop,desktopindex) in desktopApps" :key="desktopindex">
            <v-card>
                <v-img
                :src="desktop.image"
                class="white--text align-end"
                gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                height="200px"
                >
                <v-card-title>{{desktop.title}}</v-card-title>
                </v-img>
            </v-card>
        </v-col>
        </slot>
    </v-row>
</v-container>
  
</template>

<script>
       export default {
          name: "Port-folio",
          data(){
            return{
                activePortfolio:'webapp',
                webApps:[
                    {title:'Starówka', image:'https://warsawtour.pl/wp-content/uploads/2018/08/Zamkowy-Square_fot.-m.st_.-Warszawa_-PZ-Studio_Zbigniew-Panow.jpg'},
                    {title:'Łazienki', image:'https://upload.wikimedia.org/wikipedia/commons/f/fb/Pa%C5%82ac_na_wodzie_w_%C5%81azienkach_Kr%C3%B3lewskich_%28cropped%29.jpg'},
                    {title:'Pomnik', image:'https://d-art.ppstatic.pl/kadry/k/r/d1/88/5b30ffd58c575_o_full.jpg'},
                    {title:'Złote Tarasy', image:'https://i.iplsc.com/-/000DK3NUOOF20T47-C466-F4.jpg'},
                    {title:'Wiadukt', image:'https://zdm.waw.pl/wp-content/uploads/2021/07/20210630_wiadukt_Poniatowski_iluminacja-05100-scaled.jpg'},
                    {title:'Pałac Kultury', image:'https://polskazachwyca.pl/wp-content/uploads/2017/08/shutterstock_190990370-1-e1516185680833.jpg'},

                    
                ],
                mobileApps:[
                    {title:'Pomnik Czynu Rew.', image:'https://nadzory-archeologiczne.pl/wp-content/uploads/2014/03/Rzesz%C3%B3w-1024x493.jpg'},
                    {title:'Kładka', image:'https://www.skanska.pl/globalassets/externalcontent2/project/okrga-kadka-dla-pieszych-w-rzeszowie/13f68a08-8715-4b28-a772-071396bcc9a4.1.jpg?height=524&width=932&scale=both&mode=crop&bgcolor='},
                    {title:'Rynek', image:'https://erzeszow.pl/static/img/k01/WPM/rynek/min1200/r1.jpg'},
                    {title:'Galeria Rzeszów', image:'https://pliki.propertynews.pl/i/00/63/02/006302_r0_940.jpg'},
                    {title:'Pałac Lubomirskich', image:'https://erzeszow.pl/static/img/k01/atrakcje/min1200/lubomirscy_zamek.jpg'},
                    {title:'Pałacyk Letni', image:'https://d-art.ppstatic.pl/kadry/k/r/25/b1/5e5e7034b327e_o_full.jpg'},
                ],
                desktopApps:[
                    {title:'Starówka', image:'https://fajnepodroze.pl/wp-content/uploads/2019/04/stare-miasto-rynek-2_1.jpg'},
                    {title:'Smok Wawelski', image:'https://i.iplsc.com/-/000EDCLNCAHI58PU-C411.jpg'},
                    {title:'Kościół Mariacki', image:'https://polskazachwyca.pl/wp-content/uploads/2018/01/ko%C5%9Bci%C3%B3%C5%82-mariacki-krak%C3%B3w-shutterstock_667256869-e1516255860888.jpg'},
                    {title:'Bulwary Krakowskie', image:'https://cdn.galleries.smcloud.net/t/galleries/gf-zbRn-rRbF-BDcS_zdjecie-dnia-664x442-nocrop.jpg'},
                    {title:'Sukiennice', image:'https://dziendobry.tvn.pl/najnowsze/cdn-zdjecie-59jxf8-krakowskie-sukiennice-5707452/alternates/LANDSCAPE_1280'},
                    {title:'Miasto nocą', image:'https://krainawycieczek.pl/wp-content/uploads/2017/12/Krak%C3%B3w-noc%C4%85.jpg'},
                ]
            }
          }
}
</script>

<style scoped></style>