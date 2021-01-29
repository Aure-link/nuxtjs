<template>
  <div class="work">
    <div class="container">
      <h1 class="title">Mes derniers travaux</h1>
      <div class="allWork">
        <div class="line">
          <div
            v-for="project in projects"
            :key="project.id"
            @click:
            class="bloc"
          >
            <a v-bind:href="project.link">
              <div class="filter"></div>
              <img
                v-bind:src="require(`~/assets/img/${project.img}.png`)"
                class="bloc-img"
              />
              <div class="topInfo">
                <div class="date">
                  <i class="fa fa-calendar" aria-hidden="true"></i>
                  {{ project.date }}
                </div>
              </div>
              <div class="info">
                <h2>{{ project.title }}</h2>
              </div>
            </a>
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
.work {
  margin-top: 60px;
  margin-bottom: 60px;
  .title {
    text-align: center;
    margin-bottom: 50px;
    color: #01224f;
  }
  .allWork {
    display: flex;
    .line {
      display: flex;
      flex-direction: row;
      width: 100%;
      margin-bottom: 30px;
      .bloc {
        display: flex;
        width: 100%;
        justify-content: center;
        height: 400px;
        background-size: cover;
        margin: 0 15px;
        cursor: pointer;
        position: relative;
        overflow: hidden;
        &:hover {
          .info {
            opacity: 1;
            height: 20%;
          }
          .topInfo {
            opacity: 1;
            height: 15%;
          }
        }
        .filter {
          background: #2e0e0a;
          width: 100%;
          height: 100%;
          position: absolute;
          opacity: 0.5;
          transition: all 0.2s;
          z-index: 2;
          left: 0;
          &:hover {
            background-color: transparent;
          }
        }
        .bloc-img {
          width: 100%;
          height: 100%;
          object-fit: cover;
          object-position: top;
        }
        .info {
          position: absolute;
          display: flex;
          align-items: center;
          justify-content: center;
          color: #000;
          z-index: 1;
          font-size: 20px;
          background-color: #fff;
          width: 100%;
          height: 0;
          bottom: 0;
          left: 0;
          opacity: 0;
          transition: ease 0.5s;
          border: 1px solid #ccc;
          border-top: 1px solid rgba(204, 204, 204, 0.5);
          box-sizing: border-box;
          padding: 10px 15px;
          text-align: center;
        }
        .topInfo {
          background-color: #fff;
          display: flex;
          align-items: center;
          position: absolute;
          top: 0;
          right: 0;
          height: 0;
          opacity: 0;
          padding: 10px;
          transition: ease 0.5s;
          border: 1px solid #ccc;
          border-bottom: 1px solid rgba(204, 204, 204, 0.5);
          box-sizing: border-box;
          .date {
            display: flex;
            flex-direction: column;
            align-items: center;
            .fa-calendar {
              margin-bottom: 10px;
            }
          }
        }
      }
      @media screen and (max-width: 800px) {
        flex-direction: column;
        .bloc {
          margin: 0 auto;
          width: 90%;
          margin-bottom: 35px;
          height: 250px;
          .filter {
            background-color: transparent;
          }
          .topInfo {
            opacity: 1;
            height: 25%;
          }
          .info {
            opacity: 1;
            height: 20%;
          }
        }
      }
    }
    .line.visible {
      display: flex !important;
    }
    .more {
      text-align: center;
      margin-bottom: 30px;
      .button {
        display: inline-flex;
        padding: 10px 20px;
        background-color: rgba(1, 34, 79, 0.1);
        outline: 1px solid rgba(1, 34, 79, 0.1);
        outline-offset: 3px;
        cursor: pointer;
        transition: 0.2s;
        &:hover {
          background-color: #01224f;
          color: #fff;
        }
      }
    }
  }
}
</style>