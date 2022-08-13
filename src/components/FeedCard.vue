<template>
  <v-col
    cols="12"
    :md="size === 2 ? 6 : size === 3 ? 4 : undefined"
  >
    <base-card
      color="grey lighten-1"
      dark
      href="#!"
      class="rounded-lg"

    >
    
      <v-img
        v-if="value.type == 'image'"
        :src="require(`@/assets/articles/${value.hero}`)"
        height="100%"
        gradient="rgba(0, 0, 0, 0), rgba(0, 0, 0, .42)"
        contain
      >
        <v-row
          class="fill-height text-right ma-0"
        >
          <v-col cols="12">
            <v-chip
              class="text-uppercase ma-0"
              color="primary"
              label
              small
            >
            {{ value.title }}
            
            </v-chip>
          </v-col>

        </v-row>
      </v-img>
      <div class="text-center " v-else>
        <v-chip
            class="text-uppercase ma-0 absolute"
            color="primary"
            label
            small
          >
          {{ value.title }}
          
          </v-chip>
        <video controls autoplay>
          <source :src="require(`@/assets/articles/${value.hero}`)" type="video/mp4">
        </video>
      </div>
    </base-card>
  </v-col>
</template>

<script>
  export default {
    name: 'FeedCard',
    components: {
    },
    props: {
      size: {
        type: Number,
        required: true,
      },
      value: {
        type: Object,
        default: () => ({}),
      },
    },
  }
</script>

<style>
.v-image__image {
  transition: .3s linear;
}
.bg-white{
  background-color: white;
}
.absolute{
  position: absolute;
}
</style>
