<template>
    <v-container class="pt-15">
        <v-row>
            <v-col lg="6">
                <img src="https://cdn.discordapp.com/attachments/808637296286892082/992154302204366858/62083-journey-route-planning.gif" alt="car" width="500" height="500" class="d-none d-sm-flex">
                <img src="https://cdn.discordapp.com/attachments/808637296286892082/992154302204366858/62083-journey-route-planning.gif" alt="car" width="300" height="300" class="d-flex d-sm-none ml-10">
            </v-col>
            <v-col lg="6">
                <v-subheader class="textmain d-none d-sm-flex">O nas!</v-subheader>
                <v-subheader class="textmain d-flex d-sm-none justify-center">O nas!</v-subheader>
                <br>
                <p class="p black--text">Jesteśmy dwójką studentów Wyższej Szkoły Informatyki i Zarządzania w Rzeszowie. Stworzyliśmy tę stonę dla osób, które potrzebują codziennej dawki informacji na temat Naszego kraju - Polski. Nasz świat pomimo tak ogrmomnego kilometrarza, zawiera jednak stosunkowo niewiele tak pięknych miejsc jak Polska - tam, gdzie z wysokich gór można udac się nad Morze Bałtyckie i doznać tamtejszej bryzy. <br>Na naszej stronie:</p>

            <v-list>
                <v-list-item>
                    <br><br>
                    <v-icon color="teal accent-4" class="mr-3">mdi-check-all</v-icon>
                    <v-list-item-subtitle class="black--text">Jako obcokrajowiec możesz eksplorować naszą <br>
                        stronę w poszukiwaniu informacji,na temat <br>naszych pięknych miast,
                        bo wtedy odkryjesz <br>nowe miejsca, które zwiedzisz, i doznasz <br>
                        wspaniałych widoków i emocji!</v-list-item-subtitle>
                </v-list-item>
                <br>
                <v-list-item>
                    <v-icon color="teal accent-4" class="mr-3">mdi-check-all</v-icon>
                    <v-list-item-subtitle class="black--text">Jako mieszkaniec naszego kraju,<br>
                        możesz sprawdzić stan pogody dla danego miasta,<br>
                        bo wtedy możesz odpowiednio przygotować się<br>do wyjścia na zewnatrz!</v-list-item-subtitle>
                </v-list-item>
                <br>
                <v-list-item>
                    <v-icon color="teal accent-4" class="mr-3">mdi-check-all</v-icon>
                    <v-list-item-subtitle class="black--text">Jako artysta,<br>
                     możesz przejżeć galerię z największych miast<br> w Poslce,
                     bo wtedy możesz złapać nowe inspiracje!</v-list-item-subtitle>
                </v-list-item>
            </v-list>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
export default {
    name: "O-nas"
}
</script>

<style scoped>

.textmain
{font-size: 60px;
    font-weight: bold;
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    color:#444}
    
    .p{
        color: #444444ba;
        text-align: justify;
    }
</style>