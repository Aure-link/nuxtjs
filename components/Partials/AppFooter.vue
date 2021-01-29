<template>
  <div class="footer">
    <div class="container">
      <div class="left" id="copyright">
        &copy; Aurélien GUILLIET - {{ new Date().getFullYear() }}
      </div>
      <div class="right">
        <ul>
          <li>
            <a
              @mouseover="hover = true"
              @mouseleave="hover = false"
              href="https://github.com/Aure-link/"
              target="_blank"
            >
              <img
                v-if="!hover"
                src="~assets/img/github_icon.svg"
                class="icon"
                alt=""
              />
              <img
                v-if="hover"
                src="~assets/img/github_icon_hover.svg"
                class="icon"
                alt=""
              />
            </a>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      hover: false,
    };
  },
};
</script>

<style lang="scss">
.footer {
  background-color: rgba(1, 34, 79, 0.1);
  .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 20px 0;
    .right {
      ul {
        display: flex;
        flex-direction: row;
        li {
          margin-right: 15px;
          &:last-child {
            margin-right: 0;
          }
          a {
            color: #01224f;
            font-size: 17px;
            transition: 0.2s;
            position: relative;
            &:hover {
              color: #e8371a;
            }
            .icon {
              width: 20px;
              transition: 0.3s;
            }
          }
        }
      }
    }
  }
}
</style>