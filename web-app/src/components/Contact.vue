<template>
  <v-container class="my-15">
    <v-row justify="center">
        <v-col lg="12" class="text-center">
            <v-subheader class="text-h4 justify-center mt-3 mb-3 d-none d-sm-flex black--text">Kontakt</v-subheader>
            <p class="d-none d-sm-flex justify-center black--text">Wpisz swoje dane poniżej by się z nami skontakować</p>
        </v-col>
        <v-col lg="6">
<iframe class="d-none d-sm-flex" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d5035856.899819962!2d19.134378599999998!3d51.953750549999995!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x47009964a4640bbb%3A0x97573ca49cc55ea!2sPolska!5e0!3m2!1spl!2spl!4v1656530158091!5m2!1spl!2spl" width="100%" height="100%" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
<iframe class="iframe d-flex d-sm-none" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d5035856.899819962!2d19.134378599999998!3d51.953750549999995!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x47009964a4640bbb%3A0x97573ca49cc55ea!2sPolska!5e0!3m2!1spl!2spl!4v1656530158091!5m2!1spl!2spl" width="100%" height="100%" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe> 
        </v-col>
        <v-col lg="6">
<v-form ref="form" lazy-validation>
    <v-text-field
      v-model="contactInfo.name"
      :counter="10"
      label="Imię"
      required
    ></v-text-field>

    <v-textarea label="Wiadomość" v-model="contactInfo.message">

    </v-textarea>

    <v-text-field
      v-model="contactInfo.email"
      label="E-mail"
      required
    ></v-text-field>

    <v-btn color="teal lighten-1" class="mr-4 white--text">
      Wyślij
    </v-btn>
  </v-form>
        </v-col>
        </v-row>
        </v-container>
</template>

<script>
export default {
    name:"Cont-act",
    data(){
        return{
        contactInfo:{}
    }
    }
}
</script>

<style scoped>

.iframe{
  width:200px;
  margin-right:20px;
}

</style>