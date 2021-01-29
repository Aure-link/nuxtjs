<template>
  <div class="left">
    <div class="logo">
      <NuxtLink to="/">Aurélien</NuxtLink>
    </div>
  </div>
</template>

<style lang="scss">
.navbar {
  .left {
    width: 10%;
    display: inline-flex;
    align-items: flex-start;
    .logo {
      width: 100%;
      a {
        color: #222;
        font-family: "Dosis", sans-serif;
        font-size: 22px;
        font-weight: 600;
        letter-spacing: 1px;
        text-decoration: none;
        text-transform: uppercase;
      }
    }
  }
}
@media screen and (max-width: 800px) {
  .navbar {
    .left {
      margin-left: 5%;
    }
  }
}
</style>
