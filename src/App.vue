<template>
  <!-- the header -->

  <the-header></the-header>

  <router-view></router-view>

  <!-- the footer -->

  <the-footer></the-footer>
</template>
<script>
import TheHeader from "./components/Layout/TheHeader";
import TheFooter from "./components/Layout/TheFooter";
export default {
  components: {
    TheHeader,
    TheFooter,
  },

  // watch: {
  //   $route(to, from) {
  //     console.log(to);
  //     if (from.path === "/") {
  //       this.transitionName = "drain";
  //     } else {
  //       this.transitionName = "drain";
  //     }
  //   },
  // },
};
</script>
<style lang="scss">
@import "./assets/styles/base/_base.scss";

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s ease-out;
}

// .slither-enter-active,
// .slither-leave-active {
//   transition: transform 1s;
// }

// .slither-enter,
// .slither-leave-to {
//   transform: translateX(-100%);
// }

// .slither-enter-to,
// .slither-leave {
//   transform: translateX(0);
// }

// .drain-enter-active,
// .drain-leave-active {
//   transition: transform 1s;
// }

// .drain-enter,
// .drain-leave-to {
//   transform: translateY(100%);
// }

// .drain-enter-to,
// .drain-leave {
//   transform: translateY(0);
// }
</style>
