<template>
  <div class="big-header background__one">
    <div class="game">
      <router-link class="button-game button" to="/character" @click="incrementTime">Jouer</router-link>
    </div>
  </div>
</template>

<script>
import data from "../data";

export default {
  data() {
    return {
      time: 1
    };
  },
  methods: {
    incrementTime() {
      let increment = setTimeout(this.time + 1, 100);
      localStorage.setItem(time, increment);
    }
  }
};
</script>
