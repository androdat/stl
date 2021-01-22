<template>
  <div>
    <div class="menu-ul">
      <ul>
        <li v-for="(navLink, index) in navLinks" :key="index">
          <div
            class="menu-item "
            v-bind:class="{ menuitempressed: navLink.pressed }"
            @click="route(index)"
          >
            <ion-icon
              class="patient-management-icon"
              :name="navLink.icon"
            ></ion-icon>
            <p>{{ navLink.text }}</p>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "sideNav",
  data() {
    return {
      navLinks: [
        {
          text: "Home",
          icon: "home-outline",
          pressed: false
        },
        {
          text: "Patient Management",
          icon: "people-outline",
          pressed: false
        },

        {
          text: "Account Management",
          icon: "receipt-outline",
          pressed: false
        }
      ]
    };
  },
  methods: {
    route(x) {
      switch (x) {
        case 0:
          console.log(this.navLinks[x].pressed);
          console.log("home");
          this.navLinks[x].pressed = true;
          this.$router.push("/");
          break;
        case 1:
          console.log(this.navLinks[x].pressed);
          this.navLinks[x].pressed = true;
          console.log("patient management");
          this.$router.push("patientManagement");
          break;
        case 2:
          console.log(this.navLinks[x].pressed);
          this.navLinks[x].pressed = true;
          console.log("account management");
          this.$router.push("accountManagement");
          break;
      }
    }
  }
};
</script>

<style lang="scss" scoped></style>
