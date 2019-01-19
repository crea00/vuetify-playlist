<template>
  <!-- v-app is the Root Component we use in from Vuetify -->
  <v-app class="grey lighten-4">
    <Navbar />
  
    <!-- Here is where our other comtent is being loaded in -->
    <v-content class="mx-4 mb-4">
      <router-view></router-view>
    </v-content>

  </v-app>
</template>

<script>
import Navbar from '@/components/Navbar'

export default {
  name: 'App',
  components: { 
    Navbar
  },
  data () {
    return {
      //
    }
  }
}
</script>
