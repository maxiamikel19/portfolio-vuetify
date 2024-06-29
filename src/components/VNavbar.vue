<template>
    <nav>
        <v-toolbar
            app
            flat
            dark
            prominent
            color="indigo-accent-2"
        >
        <v-app-bar-nav-icon 
            variant="text" 
            @click.stop="drawer = !drawer"
            color="white"
        ></v-app-bar-nav-icon>

        <v-toolbar-title
            class="text-uppercase text-white"
        >
            <span class=" font-white">Max</span>
            <span>Home</span>
        </v-toolbar-title>
        <v-spacer></v-spacer>
        <v-btn flat color="white" >
            <span>Logout</span>
            <v-icon end>mdi-export</v-icon>
        </v-btn>
        </v-toolbar>

        <v-navigation-drawer app class="indigo" v-model="drawer" color="indigo-accent-2">
            <v-list>
                
                <v-list-subheader>Plain Variant</v-list-subheader>
                    <v-divider
                    ></v-divider>

                    <v-list-item
                        v-for="(item, i) in links"
                        :key="i"
                        :value="item"
                        color="primary"
                        variant="plain"
                        :to="item.route"
                        nav
                    >
                        <template v-slot:prepend>
                        <v-icon :icon="item.icon"></v-icon>
                        </template>

                        <v-list-item-title v-text="item.text"></v-list-item-title>
                    </v-list-item>
            </v-list>
        </v-navigation-drawer>
    </nav>
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