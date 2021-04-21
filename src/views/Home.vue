<template>
  <div class="home">
    <div id="bio">
      <div class="image-container mt-5" id="bio-content">
        <v-avatar size="150">
          <img src="@/assets/my.jpg" />
        </v-avatar>
        <div class="font-weight-bold py-3">
          KEVA DAM<span class="grey--text">AR GALIH</span>
        </div>
        <div class="font-weight-bold pb-3">
          <span class="grey--text">WEB DEV</span>ELOPER
        </div>
        <div>
          <a href="https://github.com/kevadamar" target="_blank">
            <v-icon color="white" class="mx-2 github-linkedin"
              >mdi-github</v-icon
            >
          </a>
          <a
            href="https://www.linkedin.com/in/keva-damar-galih-10708b190"
            target="_blank"
          >
            <v-icon color="white" class="mx-2 github-linkedin"
              >mdi-linkedin</v-icon
            >
          </a>
          <a href="mailto:kevadamarg@gmail.com" target="_blank">
            <v-icon color="white" class="mx-2 ig-email">mdi-email</v-icon>
          </a>
          <a href="https://www.instagram.com/kevadamar" target="_blank">
            <v-icon color="white" class="mx-2 ig-email">mdi-instagram</v-icon>
          </a>
        </div>
      </div>
    </div>
    <v-container>
      <v-card dark class="text-center pt-10 px-6">
        <v-layout row wrap class="pb-3">
          <v-flex xs12 sm3>
            <v-btn depressed block @click="loadComponent = 'Introduction'"
              >Tentang</v-btn
            >
          </v-flex>
          <v-flex xs12 sm3>
            <v-btn depressed block @click="loadComponent = 'Skills'"
              >Kemampuan</v-btn
            >
          </v-flex>
          <v-flex xs12 sm3>
            <v-btn depressed block @click="loadComponent = 'Education'"
              >Pendidikan</v-btn
            >
          </v-flex>
          <v-flex xs12 sm3>
            <v-btn depressed block @click="loadComponent = 'Experience'"
              >Pengalaman</v-btn
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
import Introduction from "../components/Introduction";
import Skills from "../components/Skills";
import Education from "../components/Education";
import Experience from "../components/Experience";
export default {
  name: "Home",
  components: {
    Introduction,
    Skills,
    Education,
    Experience
  },
  data() {
    return {
      loadComponent: "Introduction"
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
