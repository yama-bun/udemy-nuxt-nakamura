<template>
  <section class="container">
    <h1>{{ message }}</h1>
    <hr>
    <router-link to="/price">Price Page</router-link>
  </section>
</template>

<script>
export default {
  data() {
    return {
      message: 'Hello Nuxt.js!'
    }
  }
}
</script>

<style>
  .container {
    text-align: center;
    padding: 20px;
  }
</style>
