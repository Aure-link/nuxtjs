<template>
  <div class="navbar">
    <div class="container">
      <logo />
      <hamburger />
      <app-nav />
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.navbar {
  max-height: 80px;
  min-height: 80px;
  background-color: white;
  border-bottom: 1px solid #e7e7e7;
  display: flex;
  align-items: center;
}
@media screen and (max-width: 800px) {
  .navbar {
    display: flex;
    max-height: inherit;
    .container {
      width: 100%;
    }
  }
}
</style>