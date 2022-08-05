<template>
  <section id="feed">
    <v-sheet
      class="mx-auto"
      elevation="8"
      max-width="1200"
    >
      <v-slide-group
        v-model="model"
        class="pa-4"
        active-class="success"
        show-arrows
      >
        <v-slide-item
          v-for="n in 15"
          :key="n"
        >

        <v-img
          lazy-src="https://picsum.photos/id/11/10/6"
          height="200"
          width="200"
          src="https://picsum.photos/id/11/500/300"
          class="ma-4 rounded-lg"
        >
          <!-- <v-card
            :color="active ? undefined : 'grey lighten-1'"
            class="ma-4"
            height="200"
            width="100"
            @click="toggle"
          > -->
            <!-- <v-row
              class="fill-height"
              align="center"
              justify="center"
            >
              <v-scale-transition>
                <v-icon
                  v-if="active"
                  color="white"
                  size="48"
                  v-text="'mdi-close-circle-outline'"
                ></v-icon>
              </v-scale-transition>
            </v-row> -->
          <!-- </v-card> -->
          </v-img>
        </v-slide-item>
      </v-slide-group>
    </v-sheet>
  </section>
</template>

<script>
  export default {
    name: 'HomeAbout',
    components: {
    },
    data:() => ({
      model:null,
    })
  }
</script>
