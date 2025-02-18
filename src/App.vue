<template>
  <div id="app">
    <h1>Vue Swiper Demo</h1>
    <SwiperComponent />
  </div>
</template>

<script>
import SwiperComponent from "./components/SwiperComponent.vue";

export default {
  components: {
    SwiperComponent,
  },
};
</script>

<style>
#app {
  text-align: center;
  margin-top: 50px;
}
</style>
