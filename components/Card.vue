<template>
  <v-card outlined class="mx-5" min-height="17rem" max-width="100%">
    <v-carousel height="200" hide-delimiter-background show-arrows-on-hover>
      <v-carousel-item
        style="height: 100%"
        v-for="color in colors"
        :key="color"
      >
        <v-sheet height="100%" tile>
          <v-row class="fill-height" align="center" justify="center">
            <v-img
              class="white--text align-end"
              height="200px"
              src="https://cdn.vuetifyjs.com/images/cards/docks.jpg"
            />
            <!-- <div class="text-h2 fill-height">Slide {{ i + 1 }}</div> -->
          </v-row>
        </v-sheet>
      </v-carousel-item>
    </v-carousel>
    <!-- <v-img class="white--text align-end" height="200px" src="https://cdn.vuetifyjs.com/images/cards/docks.jpg"/> -->
    <v-card-text class="pb-5" style="height: 40%">
      <div class="text-subtitle-2">Istanbul - 12.4 km</div>

      <h4
        style="
          color: black;
          white-space: nowrap;
          text-overflow: ellipsis;
          overflow: hidden;
        "
        class="my-1"
      >
        018 Toyota Corolla 1.4 D-4D Touch Dizel Otomatik
      </h4>
      <div class="text-subtitle-2 my-1">Category</div>
      <h4
        style="
          color: black;
          white-space: nowrap;
          text-overflow: ellipsis;
          overflow: hidden;
        "
        class="my-1"
      >
        219,000 TL
      </h4>
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
