<template>
  <div class="big-header">
    <h1>Character</h1>
    <br>
    <router-link class="button" to="/game/2" @click.native.prevent="sexe('female')">Fille</router-link>
    <router-link class="button" to="/game/2" @click.native.prevent="sexe('male')">Garçon</router-link>
  </div>
</template>

<script>
import Sexe from "../sexe.js";
export default {
  methods: {
    sexe(sexe) {
      Sexe.getSexe(sexe);
    }
  }
};
</script>
