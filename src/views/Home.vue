<template>
  <div id="home">
    <banner />

    <articles></articles>

    <timeline/>

    <subscribe />

    <social />
  </div>
</template>

<script>
  export default {
    name: 'Home',

    components: {
      Timeline: () => import('@/components/home/Timeline'),
      Articles: () => import('@/components/home/Articles'),
      Banner: () => import('@/components/home/Banner'),
      Social: () => import('@/components/home/Social'),
      Subscribe: () => import('@/components/home/Subscribe'),
    },
  }
</script>
