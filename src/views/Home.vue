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
        <h1>This is Home</h1>
      </div>
    </div>
  </div>
</template>

<script>
import logo from "../components/logo.vue";
import topNav from "../components/topNav.vue";
import sideNav from "../components/sideNav.vue";

// import sideNav from '@/components/sideNav.vue'

export default {
  name: "Home",
  components: {
    logo,
    topNav,
    sideNav
  },

  methods: {
    route(x) {
      switch (x) {
        case 1:
          console.log("home");
          this.$router.push("Home");
          break;
        case 2:
          console.log("patient management");
          this.$router.push("patientManagement");
          break;
        case 3:
          console.log("account management");
          this.$router.push("accountManagement");
          break;
      }
    }
  }
};
</script>
