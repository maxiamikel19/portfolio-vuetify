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
            
        </v-navigation-drawer>
    </nav>
</template>

<script>
    export default {
        name: 'VNavbar',
        data(){
            return{
                drawer: false
            }
        }
    }
</script>

<style scoped>

</style>