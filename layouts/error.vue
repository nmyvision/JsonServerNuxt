<template>
  <section class="container">
    <img src="../assets/img/logo.png" alt="Nuxt.js Logo" class="logo" >
    <h1 class="title">
      {{ error.statusCode }}
    </h1>
    <h2 class="info">
      {{ error.message }}
    </h2>
    <nuxt-link v-if="error.statusCode === 404" class="button" to="/" >
      Homepage
    </nuxt-link>
  </section>
</template>
<script>
export default {
  props: ["error"] // eslint-disable-line vue/require-prop-types
}
</script>

<style scoped>
.title {
  margin-top: 15px;
  font-size: 5em;
}
.info {
  font-weight: 300;
  color: #9aabb1;
  margin: 0;
}
.button {
  margin-top: 50px;
}
</style>
