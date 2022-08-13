<template>
  <div id="home">
    <banner id="banner" />
    <div :class="[{blur:isBlur}, 'secret-part']">
      <articles id="article"></articles>

      <timeline id="timeline"/>

      <subscribe id="subcribe"/>

      <social id="social"/>
    </div>
  </div>
</template>

<script>
const birthDay = new Date(2022, 8, 16).getTime();
  export default {
    name: 'Home',
    computed:{
      isBlur(){
        let today = new Date().getTime();
        if(today === birthDay || location.hostname == 'localhost'){
          return false;
        }
        return true;
      }
    },
    components: {
      Timeline: () => import('@/components/home/Timeline'),
      Articles: () => import('@/components/home/Articles'),
      Banner: () => import('@/components/home/Banner'),
      Social: () => import('@/components/home/Social'),
      Subscribe: () => import('@/components/home/Subscribe'),
    },
  }
</script>

<style scoped>
.secret-part{
  margin-top: 10px;
  /* background-image: url('https://cdn-icons-png.flaticon.com/512/61/61457.png'); */
}
.blur{
  filter: blur(100px);
  -webkit-filter: blur(100px);
}
</style>
