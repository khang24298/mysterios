<template>
  <v-timeline class="container">
    <v-timeline-item
      v-for="n in 4"
      :key="n"
      large
    >
      <template v-slot:icon>
        <v-avatar>
          <img src="https://i.pravatar.cc/64">
        </v-avatar>
      </template>
      <template v-slot:opposite>
        <span>Tus eu perfecto</span>
      </template>
      <v-card class="elevation-2">
        <v-card-title class="text-h5">
          <v-btn
            class="ma-2"
            color="primary"
            @click="expand = !expand"
          >
            Expand Transition
          </v-btn>
        </v-card-title>
        <v-expand-x-transition>
          <v-card
            v-show="expand"
            height="auto"
            width="300"
            class="mx-auto"
          >
            <v-img :src="'http://i.pravatar.cc/'+(n*100)"/>
            <v-card-text>
              Lorem ipsum dolor sit amet, no nam oblique veritus. Commune scaevola imperdiet nec ut, sed euismod convenire principes at. Est et nobis iisque percipit, an vim zril disputando voluptatibus, vix an salutandi sententiae.
            </v-card-text>
          </v-card>
        </v-expand-x-transition>
      </v-card>
    </v-timeline-item>
  </v-timeline>
</template>

<script>
  export default {
    name: 'Timeline',
    data: () => ({
      expand: false,
    })
  }
</script>
