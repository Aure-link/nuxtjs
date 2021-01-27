<template>
  <div class="right">
    <ul>
      <li>
        <NuxtLink to="/">Accueil</NuxtLink>
      </li>
      <li>
        <NuxtLink to="/a-propos">A propos de moi</NuxtLink>
      </li>
      <li>
        <NuxtLink to="/portfolio">Portfolio</NuxtLink>
      </li>
      <li>
        <NuxtLink to="/mes-competences">Mes compétences</NuxtLink>
      </li>
      <li>
        <NuxtLink to="/contact">Contact</NuxtLink>
      </li>
    </ul>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.right {
  width: 89%;
  display: inline-flex;
  align-items: flex-end;
  justify-content: flex-end;
  ul {
    li {
      display: inline-block;
      margin-right: 30px;
      text-transform: uppercase;
      a {
        font-family: "Lato", sans-serif;
        font-size: 13px;
        font-weight: 400;
        position: relative;
        text-transform: uppercase;
        color: #01224f;
        transition: 0.2s;
        &:hover {
          color: #e8371a;
        }
      }
      &:last-child {
        margin-right: 0;
      }
    }
    li.dropdown {
      position: relative;
      a {
        display: flex;
        flex-direction: column;
        align-items: center;
        cursor: pointer;
      }
    }
    .selection {
      display: none;
      position: absolute;
      background-color: #fff;
      top: 77px;
      right: -51px;
      padding: 5px 30px;
      border: 1px solid rgba(0, 0, 0, 0.3);
      border-top: none;
      ul {
        display: flex;
        flex-direction: column;
        justify-content: center;
        li {
          padding: 10px 20px;
          margin: 0;
          display: initial;
        }
      }
    }
  }
}
@media screen and (max-width: 800px) {
  .right {
    ul {
      li {
        display: block;
        padding: 10px 0;
        text-align: center;
        margin: 0;
        &:first-child {
          margin-top: 20px;
        }
        &:last-child {
          padding-bottom: 30px;
        }
      }
    }
    display: none;
    width: 100%;
    background-color: #fff;
  }
}
</style>