<template>
  <v-app dark>
    <navbar></navbar>
    <v-content>
      <nuxt></nuxt>
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
