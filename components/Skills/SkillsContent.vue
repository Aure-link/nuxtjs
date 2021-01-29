<template>
  <div class="skill">
    <div class="container">
      <h1 class="title">Mes compétences</h1>
      <div class="allSkills">
        <div class="line">
          <div v-for="skill in skills" v-bind:key="skill.id" class="bloc">
            <div class="title">
              {{ skill.title }}
            </div>
            <div class="info">
              {{ skill.info }}
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { skills } from "../../content/skills.js";
export default {
  data() {
    return {
      skills,
    };
  },
};
</script>

<style lang="scss">
.skill {
  .title {
    text-align: center;
    color: #01224f;
    margin-bottom: 50px;
  }
  .allSkills {
    margin-bottom: 75px;
    .line {
      display: flex;
      flex-direction: row;
      margin-bottom: 50px;
      .bloc {
        display: flex;
        flex-direction: column;
        align-items: center;
        text-align: center;
        background-color: #fff;
        padding: 50px 25px;
        transition: all 0.6s ease 0s;
        width: 33.33%;
        &:nth-child(2) {
          margin: 0 25px;
        }
        .icons {
          font-size: 30px;
        }
        .title {
          margin: 25px 0;
          font-size: 20px;
        }
        .info {
          line-height: 25px;
        }
        &:hover {
          margin-top: -15px;
          margin-bottom: 15px;
          -webkit-box-shadow: 0 25px 45px rgba(0, 0, 0, 0.15);
          -moz-box-shadow: 0 25px 45px rgba(0, 0, 0, 0.15);
          box-shadow: 0 25px 45px rgba(0, 0, 0, 0.15);
        }
      }
    }
  }
}
@media screen and (max-width: 800px) {
  .skill {
    .title {
      margin-bottom: 0px;
    }
    .allSkills {
      margin-bottom: 30px;
      .line {
        flex-direction: column;
        width: 100%;
        margin: auto;
        margin-bottom: 25px;
        .bloc {
          padding: 25px 10px;
          width: 100%;
          box-sizing: border-box;
          &:nth-child(2) {
            margin: 0;
          }
        }
      }
    }
  }
}
</style>