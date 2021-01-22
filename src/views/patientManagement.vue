<template>
  <div>
    <div class="grid-container">
      <div class="grid-item grid-item-1">
        <logo />
      </div>
      <div class="grid-item grid-item-2">
        <topNav />
      </div>
      <div class="grid-item grid-item-3">
        <sideNav />
      </div>
      <div class="grid-item grid-item-4">
        <h1>This is Patient Management</h1>
      </div>
    </div>
  </div>
</template>

<script>
import logo from "../components/logo.vue";
import topNav from "../components/topNav.vue";
import sideNav from "../components/sideNav.vue";

export default {
  name: "patienManagement",
  components: {
    logo,
    topNav,
    sideNav
  }
};
</script>

<style lang="scss" scoped></style>
