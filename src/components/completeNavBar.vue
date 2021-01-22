<template>
  <div>
    <div class="grid-container">
      <div class="grid-item grid-item-1">
        <div class="absolute">
          <p class="hport-logo">hport</p>
        </div>
        <div class="border"></div>
      </div>
      <div class="grid-item grid-item-2">
        <div class="title">
          <p>Patient Management</p>
        </div>

        <div class="profile">
          <div class="profile-text">
            <p class="profile-text-p-one">Jones Fredinand</p>
            <p class="profile-text-p-two">xyz hospital</p>
          </div>
          <div class="profile-img"></div>
          <ion-icon
            class="profile-downarrow"
            name="chevron-down-outline"
          ></ion-icon>
        </div>
      </div>
      <div class="grid-item grid-item-3">
        <div class="menu-ul">
          <ul>
            <li>
              <div class="menu-item" @click="route(1)">
                <ion-icon
                  class="patient-management-icon"
                  name="home-outline"
                ></ion-icon>
                <p>Home</p>
              </div>
            </li>
            <li>
              <div class="menu-item" @click="route(2)">
                <ion-icon
                  class="patient-management-icon"
                  name="people-outline"
                ></ion-icon>
                <p>Patient Management</p>
              </div>
            </li>
            <li>
              <div class="menu-item" @click="route(3)">
                <ion-icon
                  class="patient-management-icon"
                  name="receipt-outline"
                ></ion-icon>
                <p>Account Management</p>
              </div>
            </li>
          </ul>
        </div>
      </div>
      <div class="grid-item grid-item-4">
        <h1>this is</h1>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
// import sideNav from '@/components/sideNav.vue'

export default {
  name: "navBar",
  // components: {
  //   sideNav
  // }

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
