<template>
  <div class="portfolioItem-container">
    <div class="moreInfo">
      <div class="container">
        <div
          v-for="project in projects"
          v-if="$route.params.id == project.id"
          class="content"
        >
          <div class="left">
            <div class="explication">
              <div class="title animated lightSpeedIn">{{ project.title }}</div>
              <div class="info">
                {{ project.text }}
              </div>
              <div class="myWork info">
                {{ project.resume }}
              </div>
              <div v-html="project.description" class="desc info"></div>

              <div v-if="project.livrables" class="myWork info livrables">
                Les livrables :
              </div>
              <div v-html="project.livrables" class="livrables info"></div>
            </div>
            <div class="plus">
              <a class="button" v-bind:href="project.link" target="_blank"
                >Voir le site</a
              >
            </div>
          </div>
          <div class="right">
            <img
              v-bind:src="require(`~/assets/img/${project.img}.png`)"
              class="img"
            />
            <div class="infos">
              <div class="title"></div>
              <div class="date"></div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { projects } from "../../content/projects.js";
export default {
  data() {
    return {
      projects,
    };
  },
};
</script>

<style lang="scss">
.moreInfo {
  .content {
    display: flex;
    justify-content: space-between;
    margin: 50px 0;
    .left {
      width: 100%;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      margin-right: 50px;
      .title {
        font-size: 25px;
        margin: 10px 0 30px 0;
        color: #01224f;
      }
      .info {
        line-height: 25px;
        margin-bottom: 25px;
      }
      .info.livrables {
        margin-bottom: 5px;
      }
      .myWork {
        &:before {
          content: "\f105";
          font-family: FontAwesome;
          font-size: 20px;
          font-weight: bold;
          text-decoration: inherit;
          margin-right: 10px;
          color: #01224f;
        }
      }
      .button {
        display: inline-flex;
        padding: 10px 20px;
        background-color: rgba(1, 34, 79, 0.1);
        outline: 1px solid rgba(1, 34, 79, 0.1);
        outline-offset: 3px;
        cursor: pointer;
        transition: 0.2s;
        margin-top: 25px;
        &:hover {
          background-color: #01224f;
          color: #fff;
        }
      }
    }
    .right {
      img {
        width: 100%;
        height: auto;
        object-position: top;
      }
      width: 100%;
      height: 650px;
      overflow-y: scroll;
      outline: 1px solid rgba(1, 34, 79, 0.1);
      outline-offset: 3px;
      iframe {
        display: inline-flex;
        padding: 3px 3px;
        outline: 1px solid rgba(1, 34, 79, 0.1);
        outline-offset: 3px;
        cursor: pointer;
        transition: 0.2s;
      }
    }
  }
}
@media screen and (max-width: 800px) {
  .moreInfo {
    .content {
      display: block;
      .left {
        margin-right: 0;
        margin-bottom: 50px;
        .button {
          float: right;
        }
      }
    }
  }
  .contactMe {
    .lastLineContact {
      flex-direction: column;
      align-items: flex-start;
    }
  }
}
</style>