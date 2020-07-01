<template>
  <v-app light>
    <navbar></navbar>
    <v-content>
      <v-app>
        <nuxt></nuxt>
      </v-app>   
    </v-content>
  </v-app>
</template>

<script>
import navbar from '../components/layoutComponents/navbar.vue'
export default {
  components: {
    navbar
  }
}
</script>
