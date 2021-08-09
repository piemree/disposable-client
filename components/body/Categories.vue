<template>
  <v-sheet class="mx-auto my-5 d-flex justify-center">
    <v-slide-group class="d-flex justify-center" multiple show-arrows>
      <v-slide-item v-for="n in 10" :key="n">
        <div>
          <v-btn
            :style="{ transform: `scale(${scaleCoefficient})` }"
            class="mx-2 white--text"
            color="red"
            width="129px"
            height="156px"
            depressed
            rounded
          >
            <v-icon size="2rem"> mdi-camera </v-icon>
          </v-btn>
          <p
            class="
              grey--text
              text--darken-4
              font-weight-regular
              my-1
              text-center text-subtitle-2
            "
          >
            Categorie name
          </p>
        </div>
      </v-slide-item>
    </v-slide-group>
  </v-sheet>
</template>
<script>
export default {
  data() {
    return {}
  },
  computed: {
    scaleCoefficient() {
      if (
        this.$vuetify.breakpoint.name === 'xs' ||
        this.$vuetify.breakpoint.name === 'sm'
      ) {
        return 0.8
      }
      return 1
    },
  },
}
</script>

<style></style>
