<template>
  <v-app>
    <v-navbar />
    <v-main class="mx-4 mb-4"  >
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>
import VNavbar from '@/components/VNavbar.vue'

export default {
  name: 'App',
  components: { VNavbar,  },

  data: () => ({
    //
  }),
}
</script>

<style>

  *{
    margin: 0px;
    padding: 0px;
    box-sizing: border-box;
  }
  .main{
    border: solid 1px;
    width: 90%;
    margin: 0 auto;
    margin-top: 2em;
    border-radius: .5em;
    padding: 1em;
    margin-bottom: 0em;
    height: 100dvh;
    overflow-y: scroll;
  }

  .main-title{
    color: #BF360C;
    font-size: 1.3em;
    text-transform: uppercase;
    font-weight: 400;
  }
</style>
