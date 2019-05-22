<template>
  <div class="big-header">
    <div class="question">
      <p>Voici tes statistiques : &nbsp;</p>
      <br>
      <p v-if="step == 29">Tu as survécu pendant 30 etapes étapes</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      step: localStorage.getItem("step")
    };
  }
};
</script>
