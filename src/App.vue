<template>
  <div id="app">
    <!-- <sideNav :nav-links="navLinks" /> -->

    <!-- <div class="grid-container">
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
              <div class="menu-item">
                <ion-icon class="patient-management-icon" name="people-outline"></ion-icon>
                <p>Patient Management</p>
              </div>
            </li>
                 <li>
              <div class="menu-item">
                <ion-icon class="patient-management-icon" name="receipt-outline"></ion-icon>
                <p>Account Management</p>
              </div>
            </li>
          </ul>
        </div>
      </div>
      <div class="grid-item grid-item-4"></div>
    </div> -->
    <router-view />
  </div>
</template>

<script>
// import sideNav from "@/components/sideNav";
export default {
  components: {
    // sideNav
  },
  data() {
    return {
      navLinks: [
        {
          text: "Contact",
          path: "/contact",
          icon: "ion-ios-megaphone"
        },
        {
          text: "About",
          path: "/about",
          icon: "ion-ios-business"
        },
        {
          text: "Blog",
          path: "/blog",
          icon: "ion-ios-bonfire"
        },
        {
          text: "Portfolio",
          path: "/portfolio",
          icon: "ion-ios-briefcase"
        }
      ]
    };
  }
};
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
}
html,
body {
  background-color: #f8f9fb;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

.grid-container {
  display: grid;
  grid-template-columns: 20vw 80vw;
  grid-template-rows: 8vh 92vh;
  column-gap: 2px;
}

.grid-item-1 {
  grid-column-start: 1;
  grid-column-end: 2;
  grid-row-start: 1;
  grid-row-end: 2;
  // border: solid red;
  position: relative;
  background-color: white;
  // border-bottom: solid #CECECE;
  // box-shadow: 1px 1px 4px rgba(0, 0, 0, 0.25);
  box-shadow: 1px 4px 4px rgba(0, 0, 0, 0.25);
}
.border {
  width: 90%;
  border-bottom: solid 0.7px #cecece;
  position: absolute;
  top: 100%;
  left: 50%;
  z-index: 1;
  transform: translate(-50%, -50%);
}
// .grid-item-1:after {
//     content: ""; /* This is necessary for the pseudo element to work. */
//     display: block; /* This will put the pseudo element on its own line. */
//     margin: 0 auto; /* This will center the border. */
//     width: 50%; /* Change this to whatever width you want. */
//     padding-top: 20px; /* This creates some space between the element and the border. */
//     border-bottom: 1px solid black; /* This creates the border. Replace black with whatever color you want. */
// }

.grid-item-2 {
  width: 100%;
  grid-column-start: 2;
  grid-column-end: 3;
  grid-row-start: 1;
  grid-row-end: 2;
  // border: solid green;
  position: relative;
  background-color: white;
  box-shadow: 1px 1px 4px rgba(0, 0, 0, 0.25);
}

.grid-item-3 {
  grid-column-start: 1;
  grid-column-end: 2;
  grid-row-start: 1;
  grid-row-start: 2;
  position: relative;
  //border: solid purple;
  background-color: white;
  box-shadow: 1px 4px 4px rgba(0, 0, 0, 0.25);
}

.grid-item-4 {
  grid-column-start: 2;
  grid-column-end: 3;
  grid-row-start: 2;
  grid-row-end: 3;

  // border: solid sienna;
}

.absolute {
  width: fit-content;
  height: fit-content;

  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
.hport-logo {
  font-family: "Poppins", sans-serif;
  font-style: normal;
  font-weight: normal;
  font-size: 42px;
  line-height: 54px;
  color: #2c9cee;
  text-align: center;
  cursor: pointer;
}

.title {
  //border: dotted rebeccapurple;
  width: fit-content;
  height: fit-content;
  position: absolute;
  top: 50%;
  left: 2%;
  transform: translate(0%, -50%);
  p {
    font-family: "Poppins", sans-serif;
    font-style: normal;
    font-weight: normal;
    font-size: 24px;
    line-height: 20px;
    color: #252733;
  }
}
.profile {
  // border: solid dodgerblue;
  width: fit-content;
  height: fit-content;
  position: absolute;
  top: 50%;
  right: 2%;
  transform: translate(0%, -50%);
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.profile-text {
  margin-right: 5px;
  p {
    text-align: right;
    font-family: "Poppins", sans-serif;
    font-style: normal;
    font-weight: normal;
    font-size: 18px;
    line-height: 20px;
    color: #252733;
  }
}

.profile-text-p-two {
  font-size: 14px !important ;
}
.profile-img {
  margin-right: 5px;
  width: 40px;
  height: 40px;
  border: solid red;
  border-radius: 50px;
}

.profile-downarrow {
  font-size: 25px;
  // margin-top: 10px;
}

.menu-ul {
  // border: dotted green;
  width: 90%;
  position: absolute;
  top: 3%;
  left: 50%;
  transform: translate(-50%, 0%);

  ul {
    list-style-type: none;
  }
  li {
    padding-bottom: 10px;
  }
}
.menu-item:hover {
  cursor: pointer;
  background: #e3f2fd;
  p {
    color: #2c9cee;
  }

  .patient-management-icon {
    color: #2c9cee;
  }
}
.menu-item {
  height: 45px;
  // background: #e3f2fd;
  border-radius: 4px;
  display: flex;
  align-items: center;
  justify-content: flex-start;

  p {
    padding-left: 20px;
    font-family: "Poppins", sans-serif;
    font-style: normal;
    font-weight: normal;
    font-size: 18px;
    line-height: 20px;
    color: black;
  }
}

.patient-management-icon {
  padding-left: 10px;
  font-size: 34px;
  color: black;
}

.menuitempressed {
  cursor: pointer;
  background: #e3f2fd;
  p {
    color: #2c9cee;
  }

  .patient-management-icon {
    color: #2c9cee;
  }
}
</style>
