<template>
  <v-row justify="center" align="center">
    <v-col lg="8" md="10">
      <div class="fill-height red">test</div>
    </v-col>
    <div style="position: absolute; left: 50%; bottom: 0">
      <v-btn
        class="hidden-md-and-up"
        style="bottom: 2rem; left: -50%; position: relative"
        width="8rem"
        height="3rem"
        elevation="0"
        rounded
        color="error"
      >
        <v-icon left> mdi-camera </v-icon>
        <span class="font-weight-bold">Sell</span>
      </v-btn>
    </div>
  </v-row>
</template>
<script>
export default {
  data: () => ({}),
}
</script>
