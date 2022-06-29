<template>
<v-container class="my-15">
    <v-row justify="center">
        <v-col lg="12" class="text-center">
            <v-subheader class="text-h4 justify-center">Portfolio</v-subheader>
            <p>Lorem ipsum Lorem ipsum Lorem ipsum Lorem ipsum</p>
        </v-col>
        <v-col lg="12">
            <div class="text-center">
                <v-chip @click="activePortfolio = 'webapp'" :color="activePortfolio === 'webapp'? 'cyan':''" class="mx-5">Web App</v-chip>
                <v-chip @click="activePortfolio = 'mobileapp'" :color="activePortfolio === 'mobileapp'? 'cyan':''" class="mx-5">Mobile App</v-chip>
                <v-chip @click="activePortfolio = 'desktopapp'" :color="activePortfolio === 'desktopapp'? 'cyan':''" class="mx-5">Desktop App</v-chip>
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
                    {title:'Web App 1', image:'https://images.pexels.com/photos/1545743/pexels-photo-1545743.jpeg?cs=srgb&dl=pexels-yurii-hlei-1545743.jpg&fm=jpg'},
                    {title:'Web App 2', image:'https://images.pexels.com/photos/1545743/pexels-photo-1545743.jpeg?cs=srgb&dl=pexels-yurii-hlei-1545743.jpg&fm=jpg'},
                    {title:'Web App 3', image:'https://images.pexels.com/photos/1545743/pexels-photo-1545743.jpeg?cs=srgb&dl=pexels-yurii-hlei-1545743.jpg&fm=jpg'},
                    {title:'Web App 4', image:'https://images.pexels.com/photos/1545743/pexels-photo-1545743.jpeg?cs=srgb&dl=pexels-yurii-hlei-1545743.jpg&fm=jpg'},
                    {title:'Web App 5', image:'https://images.pexels.com/photos/1545743/pexels-photo-1545743.jpeg?cs=srgb&dl=pexels-yurii-hlei-1545743.jpg&fm=jpg'},
                    {title:'Web App 6', image:'https://images.pexels.com/photos/1545743/pexels-photo-1545743.jpeg?cs=srgb&dl=pexels-yurii-hlei-1545743.jpg&fm=jpg'},

                    
                ],
                mobileApps:[
                    {title:'Mobile App 1', image:'https://images.pexels.com/photos/1545743/pexels-photo-1545743.jpeg?cs=srgb&dl=pexels-yurii-hlei-1545743.jpg&fm=jpg'},
                    {title:'Mobile App 2', image:'https://images.pexels.com/photos/1545743/pexels-photo-1545743.jpeg?cs=srgb&dl=pexels-yurii-hlei-1545743.jpg&fm=jpg'},
                    {title:'Mobile App 3', image:'https://images.pexels.com/photos/1545743/pexels-photo-1545743.jpeg?cs=srgb&dl=pexels-yurii-hlei-1545743.jpg&fm=jpg'},
                    {title:'Mobile App 4', image:'https://images.pexels.com/photos/1545743/pexels-photo-1545743.jpeg?cs=srgb&dl=pexels-yurii-hlei-1545743.jpg&fm=jpg'},
                    {title:'Mobile App 5', image:'https://images.pexels.com/photos/1545743/pexels-photo-1545743.jpeg?cs=srgb&dl=pexels-yurii-hlei-1545743.jpg&fm=jpg'},
                    {title:'Mobile App 6', image:'https://images.pexels.com/photos/1545743/pexels-photo-1545743.jpeg?cs=srgb&dl=pexels-yurii-hlei-1545743.jpg&fm=jpg'},
                ],
                desktopApps:[
                    {title:'Desktop App 1', image:'https://images.pexels.com/photos/1545743/pexels-photo-1545743.jpeg?cs=srgb&dl=pexels-yurii-hlei-1545743.jpg&fm=jpg'},
                    {title:'Desktop App 2', image:'https://images.pexels.com/photos/1545743/pexels-photo-1545743.jpeg?cs=srgb&dl=pexels-yurii-hlei-1545743.jpg&fm=jpg'},
                    {title:'Desktop App 3', image:'https://images.pexels.com/photos/1545743/pexels-photo-1545743.jpeg?cs=srgb&dl=pexels-yurii-hlei-1545743.jpg&fm=jpg'},
                    {title:'Desktop App 4', image:'https://images.pexels.com/photos/1545743/pexels-photo-1545743.jpeg?cs=srgb&dl=pexels-yurii-hlei-1545743.jpg&fm=jpg'},
                    {title:'Desktop App 5', image:'https://images.pexels.com/photos/1545743/pexels-photo-1545743.jpeg?cs=srgb&dl=pexels-yurii-hlei-1545743.jpg&fm=jpg'},
                    {title:'Desktop App 6', image:'https://images.pexels.com/photos/1545743/pexels-photo-1545743.jpeg?cs=srgb&dl=pexels-yurii-hlei-1545743.jpg&fm=jpg'},
                ]
            }
          }

}
</script>

<style scoped>



</style>