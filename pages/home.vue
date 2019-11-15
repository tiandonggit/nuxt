<template>
  <div class="container">
    <h1>home</h1>
    <div>
      <button @click="index">index</button>
      <button @click="article">article</button>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    index() {
      this.$router.push({ name: "index" });
    },
    article() {
      this.$router.push({ name: "article" });
    }
  }
};
</script>

<style scoped lang="less">
  h1 {
    color: @fontColor99;
  }
</style>
