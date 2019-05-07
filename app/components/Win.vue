<template>
  <div class="big-header">
    <h1>{{ message }}</h1>
    <br>
    <router-link class="button" to="/">Go to Home</router-link>
    <router-link class="button" to="/character">Go to Character</router-link>
  </div>
</template>

<script>
export default {
  data() {
    return {
      message: 'page win'
    };
  }
};
</script>
