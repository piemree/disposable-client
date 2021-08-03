<template>
  <v-app>
    <Navigation />
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
    <v-footer :absolute="true" app>
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>
<script>
export default {}
</script>
<style scoped>
* {
  text-transform: unset !important;
}
</style>
