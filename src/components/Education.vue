<template>
  <div>
    <v-timeline>
      <v-timeline-item
        v-for="(value, i) in payloads"
        :key="i"
        :color="value.color"
        small
      >
        <template v-slot:opposite>
          <span
            :class="`title font-weight-bold ${value.color}--text`"
            v-text="value.year"
          ></span>
        </template>
        <v-card :color="value.color" dark>
          <v-card-title class="title">
            {{ value.text }}
          </v-card-title>
          <v-card-text class="white lighten-3 text--primary py-3">
            <p>{{ value.description }}</p>
          </v-card-text>
        </v-card>
      </v-timeline-item>
    </v-timeline>
  </div>
</template>
<script>
export default {
  data() {
    return {
      payloads: [
        {
          color: "pink",
          year: "2006 - 2012",
          text: "SDN JATI 4 TANGERANG",
          description:
            "Perjalanan pendidikan sekolah saya diawali di SDN JATI 4 TANGERANG selama 6 tahun."
        },
        {
          color: "cyan",
          year: "2012 - 2015",
          text: "SMPN 08 TANGERANG",
          description:
            "Kemudian melanjutkan pendidikan SMP saya di SMPN 08 TANGERANG selama 3 tahun."
        },
        {
          color: "grey",
          year: "2015 - 2018",
          text: "SMK PANCAKARYA ~ MULTIMEDIA",
          description:
            "Pada pendidikan SMK saya mengambil program studi Multimedia di SMK PANCAKARYA."
        }
      ]
    };
  }
};
</script>
