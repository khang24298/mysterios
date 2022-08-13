<template>
  <section class="banner">
    <v-carousel
        cycle
        height="auto"
        hide-delimiter-background
        show-arrows-on-hover
      >
        <v-carousel-item
          v-for="(slide, i) in 1"
          :key="i"
          class="blur"
        >
          <v-sheet
            height="100%"
          >
            <v-row
              class="fill-height"
              align="center"
              justify="center"
            >
              <base-card dark>
                <v-img
                  :src="require('@/assets/banners/banner_'+(i+1)+'.jpg')"
                  class="grey lighten-2"
                  width="100%"
                >
                  <v-row
                    class="fill-height pa-3"
                    align="center"
                  >
                    <v-col
                      cols="12"
                      md="7"
                      offset-md="5"
                    >
                    </v-col>
                  </v-row>
                </v-img>
              </base-card>
            </v-row>
          </v-sheet>
        </v-carousel-item>
    </v-carousel>
    <countdown/>
  </section>
  
  
</template>

<script>
import Countdown from './Countdown.vue';
  export default {
    name: "HomeBanner",
    components: { Countdown }
}
</script>

<style scoped>
.blur{
  filter: blur(3px);
  -webkit-filter: blur(3px);
}
</style>
