<template>
  <!-- v-app is the Root Component we use in from Vuetify -->
  <v-app>

  
    <v-content>
      <router-view></router-view>
    </v-content>

  </v-app>
</template>

<script>

export default {
  name: 'App',
  data () {
    return {
      //
    }
  }
}
</script>
