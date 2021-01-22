<template>
  <div>
    <div class="absolute" @click="route">
      <p class="hport-logo">hport</p>
    </div>
    <div class="border"></div>
  </div>
</template>

<script>
export default {
  name: "logo",

  methods: {
    route() {
      this.$router.push("/");
    }
  }
};
</script>

<style lang="scss" scoped>
.hide {
  display: none;
}
</style>
