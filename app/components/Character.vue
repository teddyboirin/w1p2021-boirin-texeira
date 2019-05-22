<template>
  <div class="big-header">
    <h1>Choisissez votre personnage</h1>
    <br>
    <div class="choices">
      <router-link class="button" to="/game/2" @click.native.prevent="sexe('female')">Fille</router-link>
      <router-link class="button" to="/game/2" @click.native.prevent="sexe('male')">Garçon</router-link>
    </div>
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
