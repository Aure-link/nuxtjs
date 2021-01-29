<template>
  <div class="slider">
    <div class="container">
      <div class="slider-info">
        <div class="info">
          <h1>Aurélien Guilliet</h1>
          <span>Développeur Front-end et UX Designer</span>
        </div>
      </div>
      <a class="js-scrollTo" href="#work"
        ><span></span><span></span><span></span
      ></a>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.slider {
  background-image: url(~assets/img/slider.jpg);
  background-attachment: fixed;
  background-size: cover;
  height: 540px;
  display: flex;
  .slider-info {
    display: flex;
    justify-content: center;
    margin-bottom: 50px;
    .info {
      outline: 1px solid #fff;
      outline-offset: 8px;
      padding: 65px;
      background-color: rgba(255, 255, 255, 0.9);
      text-align: center;
      span {
        font-size: 18px;
        font-weight: 500;
      }
    }
  }
  .js-scrollTo {
    position: relative;
    display: flex;
    margin-top: 25px;
    span {
      position: absolute;
      top: 0;
      left: 50%;
      width: 24px;
      height: 24px;
      margin-left: -12px;
      border-left: 1px solid #fff;
      border-bottom: 1px solid #fff;
      -webkit-transform: rotate(-45deg);
      transform: rotate(-45deg);
      -webkit-animation: sdb 2s infinite;
      animation: sdb 2s infinite;
      opacity: 0;
      box-sizing: border-box;
      &:nth-of-type(1) {
        -webkit-animation-delay: 0s;
        animation-delay: 0s;
      }
      &:nth-of-type(2) {
        top: 16px;
        -webkit-animation-delay: 0.15s;
        animation-delay: 0.15s;
      }
      &:nth-of-type(3) {
        top: 32px;
        -webkit-animation-delay: 0.3s;
        animation-delay: 0.3s;
      }
    }
    &:after {
      display: block;
      clear: both;
      content: "";
    }
  }
}
</style>