<template>
  <div class="container">
    <div>
      <h1 class="fr">article</h1>
    </div>
    <div>
      <button @click="index">index</button>
      <button @click="home">home</button>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    index() {
      this.$router.push({ name: "index" });
    },
    home() {
      this.$router.push({ name: "home" });
    }
  }
};
</script>

<style scoped lang="less">
  h1 {
    font-size: 50px;
  }
</style>
