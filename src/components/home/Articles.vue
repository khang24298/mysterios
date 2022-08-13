<template>
  <section id="feed" class="container">
    <h1>Character</h1>
    <v-sheet
      class="mx-auto"
      elevation="8"
      max-width="1200"
    >
      <feed>
        <slot/>
        </feed>
    </v-sheet>
  </section>
</template>

<script>
import Feed from '../Feed.vue';
  export default {
    name: 'HomeAbout',
    components: {
        Feed
    },
    data:() => ({
      model:null,
    })
  }
</script>

<style scoped>
#feed{
  border-top: 1px solid lightgrey;
}
</style>