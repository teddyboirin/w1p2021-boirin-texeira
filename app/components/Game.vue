<template>
  <div class="big-header">
    <h1 v-if="$route.params.id">{{ step.title }}</h1>
    <ul v-if="$route.params.id != 9 && $route.params.id">
      <li v-for="action in step.actions" v-bind:action="action" v-bind:key="action.title">
        <router-link class="button" :to="action.to.toString()">{{ action.title }}</router-link>
      </li>
    </ul>
    <ul v-if="$route.params.id == 9 && male == true && $route.params.id">
      <li v-for="male in step.males" v-bind:male="male" v-bind:key="male.title">
        <router-link class="button" :to="male.to.toString()">{{ male.title }}</router-link>
      </li>
    </ul>
    <ul v-else-if="$route.params.id == 9 && male == false && $route.params.id">
      <li v-for="action in step.actions" v-bind:action="action" v-bind:key="action.title">
        <router-link class="button" :to="action.to.toString()">{{ action.title }}</router-link>
      </li>
    </ul>
  </div>
</template>

<script>
import game from "../data.json";
import Sexe from "../sexe.js";

export default {
  data: function() {
    return {
      step: this.getStep(),
      male: Sexe.male
    };
  },
  watch: {
    "$route.params.id"(to, from) {
      this.step = this.getStep();
    }
  },

  methods: {
    getStep() {
      return game.steps.find(step => {
        return step.id === parseInt(this.$route.params.id, 10);
      });
    }
  }
};
</script>


