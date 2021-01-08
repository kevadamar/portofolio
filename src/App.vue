<template>
  <v-app>
    <!-- <Header/> -->
    <v-content class="black white--text pt-6">
      <transition name="animate" mode="out-in">
        <router-view></router-view>
      </transition>
    </v-content>
  </v-app>
</template>
<style scoped>
.animate-enter-active {
  animation: animate-in 200ms ease-out forwards;
}
.animate-leave-active {
  animation: animate-out 200ms ease-out forwards;
}
@keyframes animate-in {
  from {
    opacity: 0;
    transform: translateY(-100px);
  }
  to {
    opacity: 1;
    transform: translateY(0px);
  }
}
@keyframes animate-out {
  from {
    opacity: 1;
    transform: translateY(0px);
  }
  to {
    opacity: 0;
    transform: translateY(-100px);
  }
}
@keyframes identifier {
}
</style>
