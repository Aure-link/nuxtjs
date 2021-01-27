<template>
    <div class="slider">
      <img src="~/assets/img/wallpaper.jpg" alt="">
    </div>
</template>

<script>
export default {

}
</script>

<style lang="scss">
    .slider {
      height: 200px;
      width: 100%;
      overflow: hidden;
      img {
        object-fit: cover;
        object-position: center;
      }
    }
</style>