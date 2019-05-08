<template>
  <div class="big-header">
    <h1>{{ message }}</h1>
    <br>

    <router-link class="button" to="/character">Go to Character</router-link>
    <router-link class="button" to="/game">Go to Game</router-link>
    <router-link class="button" to="/win">Go to win</router-link>
    <router-link class="button" to="/loose">Go to loose</router-link>
    <router-link class="button" to="/game/1">Go to game/1</router-link>
    <router-link class="button" to="/game/2">Go to game/2</router-link>
  </div>
</template>

<script>
import data from '../../data.json';

export default {
  data() {
    return {
      message: 'Page Home'
    };
  }
};
</script>
