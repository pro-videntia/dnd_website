<template>
  <v-app light>
    <navbar></navbar>
    <v-content>
      <v-app>
        <nuxt></nuxt>
      </v-app>
    </v-content>
    <footbar></footbar>
  </v-app>
</template>

<script>
import navbar from "../components/layoutComponents/navbar.vue";
import footbar from "../components/layoutComponents/footbar.vue";
export default {
  components: {
    navbar,
    footbar,
  },
};
</script>
