<template>
  <v-row justify="center" align="center">
    <v-col align-self="center" xl="9" lg="12" md="12" sm="12" xs="12">
      <div class="fill-height">
        <h3
          class="
            grey--text
            text--darken-4
            font-weight-bold
            text-center text-subtitle-1
          "
        >
          Buy and sell secondhand and find great deals!
        </h3>
        <Categories />

        <v-row class="height:20rem" no-gutters>
          <v-col
            class="my-5 fill-height"
            v-for="n in 22"
            :key="n"
            cols="12"
            sm="6"
            md="4"
            lg="3"
          >
            <Card />
          </v-col>
        </v-row>
      </div>
    </v-col>
    <div style="position: fixed; left: 50%; bottom: 0">
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
import Categories from '@/components/body/Categories'
export default {
  components: { Categories },
  data: () => ({}),
}
</script>
