<template>
  <v-app-bar
    app
    flat
  >
    <v-app-bar-nav-icon
      class="hidden-md-and-up"
      @click="toggleDrawer"
    />

    <v-container class="mx-auto py-0">
      <v-row align="center">
          <v-img
            :src="require('@/assets/logo_recut.jpeg')"
            class="mr-5 rounded-circle"
            contain
            height="48"
            width="48"
            max-width="48"
            @click="$vuetify.goTo(0)"
          />

        <v-card-text
          class="hidden-sm-and-down d-contents"
        >
        <h1>My bất ổn girl birthday!</h1>
        </v-card-text>

        <v-spacer />

      </v-row>
    </v-container>
  </v-app-bar>
</template>

<script>
  // Utilities
  import {
    mapGetters,
    mapMutations,
  } from 'vuex'

  export default {
    name: 'CoreAppBar',

    computed: {
      ...mapGetters(['links']),
    },

    methods: {
      ...mapMutations(['toggleDrawer']),
      onClick (e, item) {
        e.stopPropagation()

        if (item.to || !item.href) return

        this.$vuetify.goTo(item.href.endsWith('!') ? 0 : item.href)
      },
    },
  }
</script>

<style scoped>
.d-contents{
  display:contents;
}
.d-contents h1{
  font-family: 'Courier New', Courier, monospace;
}
</style>
