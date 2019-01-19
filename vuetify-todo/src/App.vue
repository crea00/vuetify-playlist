<template>
  <!-- v-app is the Root Component we use in from Vuetify -->
  <v-app class="grey lighten-4">
    <Navbar />
  
    <v-content>
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
