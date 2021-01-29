<template>
  <div class="container">
    <div class="contact-part">
      <div class="info mail">
        <div class="info_top">
          <div class="icon">
            <img src="~/assets/img/mail.svg" />
          </div>
          <div class="title">Me contacter par email :</div>
        </div>
        <div class="info_bot">
          <a href="mailTo:contact@aurelienguilliet.fr">contact@aurelienguilliet.fr</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.contact-part {
    display: flex;
    justify-content: center;
    margin: 30px;
  .info {
      display: flex;
      align-items: center;
      @media screen and (max-width: 600px) {
          flex-direction: column;
      }
    .info_top {
      display: flex;
      @media screen and (max-width: 600px) {
          margin-bottom: 10px;
      }
      .icon {
        margin-right: 5px;
        img {
          width: 30px;
        }
      }
      .title {
        font-size: 22px;
      }
    }
    .info_bot {
        margin-left: 5px;
        a {
            font-size: 20px;
        }
    }
  }
}
</style>