<template>
  <div class="container">
    <div>
      <logo />
      <h1 class="title">
        nuxt
      </h1>
      <button @click="home">home</button>
      <button @click="article">article</button>
      <button @click="todos">todos</button>
    </div>
  </div>
</template>

<script>
import Logo from "~/components/Logo.vue";

export default {
  components: {
    Logo
  },
  mounted() {
    this.$nextTick(() => {
      // 页面加载上方进度条
      this.$nuxt.$loading.start();

      setTimeout(() => this.$nuxt.$loading.finish(), 1000);
    });
  },
  methods: {
    home() {
      this.$router.push({ name: "home" });
    },
    article() {
      this.$router.push({ name: "article" });
    },
    todos() {
      this.$router.push({ name: "todos" });
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
  color: @fontColorBlue;
  letter-spacing: 1px;
}
</style>
