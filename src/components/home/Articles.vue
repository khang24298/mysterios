<template>
  <section id="feed" class="container articles">
    <h1 class="m-3">Character</h1>
    <v-sheet
      class="mx-auto mt-5"
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
        Feed,
    },
    data:() => ({
      model:null,
    })
  }
</script>

<style scoped>
.articles{
  border-top: 1px solid lightgray;
}
</style>