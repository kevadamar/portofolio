<template>
  <div class="home">
    <v-container class="mx-auto">
      <v-card dark class="text-center">
        <v-layout wrap class="pb-3">
          <v-flex xs12 sm6>
            <v-btn depressed block @click="loadComponent = 'Education'"
              >Pendidikan</v-btn
            >
          </v-flex>
          <v-flex xs12 sm6>
            <v-btn depressed block @click="loadComponent = 'Experience'"
              >Pengalaman Bekerja</v-btn
            >
          </v-flex>
        </v-layout>
        <transition name="slide-in" mode="out-in">
          <component :is="loadComponent"></component>
        </transition>
      </v-card>
    </v-container>
  </div>
</template>

<script>
import Education from "./Education";
import Experience from "./Experience";
export default {
  name: "Pengalaman",
  components: {
    Education,
    Experience
  },
  data() {
    return {
      loadComponent: "Education"
    };
  }
};
</script>
<style scoped>
a {
  text-decoration: none;
}

.image-container {
  width: 100%;
  margin: auto;
  text-align: center;
}
.round {
  border-radius: 50%;
}

.slide-in-enter-active {
  animation: slideInOne 200ms ease-out forwards;
}
.slide-in-leave-active {
  animation: slideOut 200ms ease-out forwards;
}
.github-linkedin {
  animation: slideInOne 2s ease-out;
}
.ig-email {
  animation: slideInTwo 2s ease-out;
}
@keyframes slideInOne {
  from {
    opacity: 0;
    transform: translateX(-100px);
  }
  to {
    opacity: 1;
    transform: translateX(0px);
  }
}
@keyframes slideInTwo {
  from {
    opacity: 0;
    transform: translateX(100px);
  }
  to {
    opacity: 1;
    transform: translateX(0px);
  }
}
@keyframes slideOut {
  from {
    opacity: 1;
    transform: translateX(0px);
  }
  to {
    opacity: 0;
    transform: translateX(-100px);
  }
}
</style>
