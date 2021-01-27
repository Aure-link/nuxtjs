<template>
  <div class="home_container">
    <app-slider />
  </div>
</template>

<script>
import AppSlider from '../components/Home/AppSlider.vue'
export default {
  components: { AppSlider },}
</script>

<style lang="scss">
  .home_container {
    background-color: red;
    .header {
      background-color: green;
    }
  }
</style>
