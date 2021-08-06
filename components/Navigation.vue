<template>
  <nav>
    <v-navigation-drawer v-model="drawer" :bottom="mini" right app>
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar :clipped-left="clipped" fixed app min-width="350px">
      <v-row align="center"  justify="center">
        <v-col lg="8" md="10" >
          <v-row align="center" justify="space-between">
            <div class="d-flex flex justify-space-between align-center">
              <v-toolbar-items
                style="width: 100%"
                class="fill-height d-flex align-center"
              >
                <v-text-field
                  color="#5e5e5e"
                  small
                  single-line
                  v-model="search"
                  placeholder="Search"
                  outlined
                  rounded
                  dense
                  prepend-inner-icon="mdi-magnify"
                  clearable
                  hide-details
                ></v-text-field>
              </v-toolbar-items>
              <v-btn
                class="ml-3 hidden-sm-and-down"
                width="6rem"
                elevation="0"
                rounded
                color="error"
              >
                <v-icon left> mdi-camera </v-icon>
                <span class="font-weight-bold">Sell</span></v-btn
              >
             
              <v-btn
                class="ml-3"
                v-show="!$vuetify.breakpoint.xs"
                width="6rem"
                elevation="0"
                outlined
                rounded
                color="error"
                ><span class="font-weight-bold">Log In</span></v-btn
              >
              <v-btn icon @click.stop="drawer = !drawer">
                <v-icon>mdi-menu</v-icon>
              </v-btn>
            </div>
          </v-row>
        </v-col>
      </v-row>
    </v-app-bar>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      search: '',
      drawer: false,
      clipped: false,
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js',
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/',
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire',
        },
      ],
    }
  },
  computed: {
    mini() {
      switch (this.$vuetify.breakpoint.name) {
        case 'xs':
          return true
        case 'sm':
          return true
        case 'md':
          return false
        case 'lg':
          return false
        case 'xl':
          return false
      }
      return false
    },
  },
}
</script>
