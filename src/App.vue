<template>
  <v-app grey lighten-4>
    <v-navbar />
    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>
import VNavbar from '@/components/VNavbar.vue'

export default {
  name: 'App',
  components: { VNavbar },

  data: () => ({
    //
  }),
}
</script>
