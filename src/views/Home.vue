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
          <span class="grey--text">FRONTEND </span>DEVELOPER
        </div>
        <div>
          <a
            :href="item.url"
            target="_blank"
            v-for="(item, idx) in listLink"
            :key="idx"
          >
            <v-tooltip bottom>
              <template v-slot:activator="{ on, attrs }">
                <v-icon
                  color="white"
                  class="mx-2 github-linkedin"
                  v-bind="attrs"
                  v-on="on"
                  >{{ item.icon }}</v-icon
                >
              </template>
              <span>{{ item.title }}</span>
            </v-tooltip>
          </a>
          <!-- <a href="https://www.linkedin.com/in/kevadamargalih" target="_blank">
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
          <a href="https://www.instagram.com/kevadamar" target="_blank">
            <v-icon color="white" class="mx-2 ig-email">
              mdi-cloud-download
            </v-icon>
          </a> -->
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
          <!-- <v-flex xs12 sm3>
            <v-btn depressed block @click="loadComponent = 'Pengalaman'"
              >Pengalaman & Pendidikan</v-btn
            >
          </v-flex> -->
          <!-- <v-flex xs12 sm3>
            <v-btn depressed block @click="loadComponent = 'Portofolio'"
              >Portofolio</v-btn
            >
          </v-flex> -->
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
import Portofolio from "../components/Portofolio";
import Pengalaman from "../components/Pengalaman";
export default {
  name: "Home",
  components: {
    Introduction,
    Skills,
    Education,
    Experience,
    Portofolio,
    Pengalaman
  },
  data() {
    return {
      loadComponent: "Introduction",
      listLink: [
        {
          title: "Github",
          icon: "mdi-github",
          url: "https://github.com/kevadamar"
        },
        {
          title: "Linkedin",
          icon: "mdi-linkedin",
          url: "https://www.linkedin.com/in/kevadamargalih"
        },
        {
          title: "Email",
          icon: "mdi-email",
          url: "mailto:kevadamarg@gmail.com"
        },
        {
          title: "Instagram",
          icon: "mdi-instagram",
          url: "https://www.instagram.com/kevadamar"
        },
        {
          title: "Resume",
          icon: "mdi-cloud-download",
          url:
            "https://drive.google.com/file/d/19CKSUYyUUazBzw3B3PrkwYfW9zQe1Gzb/view?usp=share_link"
        }
      ]
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
