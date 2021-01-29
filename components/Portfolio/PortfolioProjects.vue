<template>
  <div class="portfolio">
    <div class="work" id="work">
      <div class="container">
        <h1 class="title">Mes travaux</h1>
        <div class="allWork">
          <div class="line">
            <div
              v-for="project in projects"
              :key="project.id"
              @click:
              class="bloc"
            >
              <router-link :to="{ path: '/portfolio/' + project.id }">
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
              </router-link>
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

<style>
</style>