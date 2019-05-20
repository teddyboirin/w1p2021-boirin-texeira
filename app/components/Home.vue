<template>
  <div class="big-header background__one">
    <div class="game">
      <router-link class="button-game" to="/character">Jouer</router-link>
    </div>
  </div>
</template>

<script>
import data from "../data.json";

export default {
  data() {
    return {
      message: "Page Home"
    };
  }
};
</script>
