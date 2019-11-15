<template>
  <div class="container">
    <div>
      <logo />
      <h1 class="title">
        nuxt-first
      </h1>
      <button @click="home">home</button>
      <button @click="article">article</button>
    </div>
  </div>
</template>

<script>
import Logo from "~/components/Logo.vue";

export default {
  components: {
    Logo
  },
  methods: {
    home() {
      this.$router.push({ name: "home" });
    },
    article() {
      this.$router.push({ name: "article" });
    }
  }
};
</script>

<style scope lang="less">
.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont,
    "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}
</style>
