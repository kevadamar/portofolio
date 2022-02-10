<template>
  <div>
    <v-timeline dense>
      <v-timeline-item
        v-for="(value, i) in payloads"
        :key="i"
        color="grey"
        small
      >
        <v-card color="white" dark>
          <v-card-title class="title black--text pb-2">
            {{ value.job }}
            <span class="grey--text font-weight-bold ml-1">
              {{ value.company }}
            </span>
          </v-card-title>
          <v-card-text class="text-left white lighten-3 text--primary pb-3">
            <p class="pb-0 subtitle-1 grey--text font-weigth-bold font-italic">
              {{ value.year }}
            </p>
            <strong>Tugas Pekerjaan :</strong>
            <ul v-for="(desc, i) in value.description" :key="i">
              <li>
                <p class="py-0 my-0">{{ desc }}</p>
              </li>
            </ul>
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
          year: "September 2021 - Now",
          job: "Frontend Web Freelance",
          company: "PT. Ayo Kreasi Teknologi",
          description: [
            "Membuat Aplikasi Sistem Informasi Pelabuhan dengan NuxtJS untuk PT. Krakatau Bandar Samudera berbasis Web.",
            "Mengimplementasikan desain UI/UX ke bentuk Aplikasi Web.",
            "Menghubungkan Frontend dan Backend dengan API."
          ]
        },

        {
          year: "Agustus 2020 - Oktober 2020",
          job: "Frontend Web Freelance",
          company: "Diginova Elektra Multimedia",
          description: [
            "Membuat Aplikasi Web PWA dengan VueJS untuk alat bantu sales berjualan produk BNI berbasis Mobile.",
            "Mengimplementasikan desain UI/UX ke bentuk Aplikasi Web.",
            "Mengimplementasikan responsive Aplikasi Web Mode Mobile dengan Vuetify.",
            "Menghubungkan Frontend dan Backend dengan API."
          ]
        },
        {
          year: "Oktober 2019 - Juni 2020",
          job: "Frontend Web Developer",
          company: "Diginova Kreasi Indonesia",
          description: [
            "Membuat Aplikasi Web dengan VueJS.",
            "Menghubungkan Frontend dan Backend dengan API."
          ]
        }
      ]
    };
  }
};
</script>
