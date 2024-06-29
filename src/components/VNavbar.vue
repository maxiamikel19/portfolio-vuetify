<template>
    <div>
      <v-navigation-drawer app class="indigo" v-model="drawer" color="indigo-accent-2">
        <v-list>
            <v-list-subheader class="text-h6 pb-2" color="lime darken-4">Plain Variant</v-list-subheader>
                <v-divider></v-divider>
                <v-list-item
                    v-for="(item, i) in links"
                    :key="i"
                    :value="item"
                    color="white"
                    variant="plain"
                    :to="item.route"
                    class="text-subtitle-1"
                    nav
                >
                <template v-slot:prepend>
                   <v-icon :icon="item.icon"></v-icon>
                </template>
                    <v-list-item-title v-text="item.text" class="text-subtitle-1"></v-list-item-title>
                </v-list-item>
            </v-list>
        </v-navigation-drawer>
        <v-app-bar flat app>
            <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
            <v-app-bar-title>
                <span class="text-deep-orange-darken-4">Max</span>
                <span>Home</span>
            </v-app-bar-title>
            <v-spacer></v-spacer>
            <v-btn small elevation="" color="">
                <span>Log out</span>
                <v-icon color="" end>mdi-exit-to-app</v-icon>
            </v-btn>
       </v-app-bar>
      </div>
  </template>
  
 <script>
    export default {
        name: 'VNavbar',
        data(){
            return{
                drawer: false,
                links:[
                    {icon:'mdi-home', text: 'Home', route: '/'},
                    {icon:'mdi-account-tie', text: 'About me', route: '/about'},
                    {icon:'mdi-folder-google-drive', text: 'Projects', route: '/projects'},
                    {icon:'mdi-card-account-mail', text: 'Contact me', route: '/contact'},
                ],
            }
        },
        methods:{
            
        }
    }
</script>

<style scoped>

</style>