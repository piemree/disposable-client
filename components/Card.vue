<template>
  <v-card :loading="loading" class="mx-5" min-height="17rem" max-width="100%">
    <v-carousel height="100%" v-model="model">
      <v-carousel-item style="height:100%" v-for="(color, i) in colors" :key="color">
        <v-sheet height="100%" :color="color" tile>
          <v-row class="fill-height" align="center" justify="center">
            <div class="text-h2 fill-height">Slide {{ i + 1 }}</div>
          </v-row>
        </v-sheet>
      </v-carousel-item>
    </v-carousel>

    <v-card-text style="height:40%">
      <div class="my-1 text-subtitle-1">Italian, Cafe</div>
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  data: () => ({
    loading: false,
    selection: 1,
    model: 0,
    colors: ['primary', 'secondary', 'yellow darken-2', 'red', 'orange'],
  }),

  methods: {
    reserve() {
      this.loading = true

      setTimeout(() => (this.loading = false), 2000)
    },
  },
}
</script>

<style></style>
