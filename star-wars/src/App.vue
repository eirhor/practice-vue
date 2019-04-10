<template>
  <v-app dark>
    <v-toolbar app scroll-off-screen clipped-right>
      <v-toolbar-side-icon @click="toggleDrawer" />
      <v-toolbar-title class="headline text-uppercase">
        vimg
      </v-toolbar-title>
      <v-spacer />
    </v-toolbar>
    <v-navigation-drawer app :mini-variant="drawer.open">
      <v-list>
        <v-list-tile-action>
          <v-icon>home</v-icon>
        </v-list-tile-action>
        <v-list-tile-title v-if="!drawer.open">Home</v-list-tile-title>
      </v-list>
    </v-navigation-drawer>

    <v-content>
      <HelloWorld/>
    </v-content>
  </v-app>
</template>

<script>

export default {
  name: 'App',
  components: {
  },
  data () {
    return {
      drawer: {
        open: false
      }
    }
  },
  methods: {
    toggleDrawer() {
      this.drawer.open = !this.drawer.open;
    }
  }
}
</script>
