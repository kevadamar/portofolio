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
          job: "Frontend Developer",
          company: "PT. Ayo Kreasi Teknologi",
          description: [
            "Implementasi BTOS Multi Purpose untuk PT Persero Batam. Mendukung BTOS Multi Purpose Port Apps untuk PT Persero Batam.",
            "Buat beberapa Prosedur dan Fungsi Penyimpanan untuk laporan kustom menggunakan SQL Server.",
            "Menangani menghasilkan laporan PDF File dari laravel.",
            "Tangani integrasi Backend laravel ke Odoo.",
            "Bangun aplikasi Port Kontainer menggunakan NuxtJS.",
            "Membangun aplikasi KIPOS Break Bulk Port untuk PT Krakatau Bandar Samudera menggunakan NuxtJS.",
            "Integrasi Frontend dan Backend KIPOS dengan API.",
            "Bangun aplikasi Multi Purpose Port menggunakan teknologi yang sama dengan Break Bulk Port.",
            "Buat komponen Filterbar yang dapat digunakan kembali, Cari Pilih, dan Skeleton Loader.",
            "Buat Helper Formating Number dan periksa akses pengguna."
          ]
        },
        {
          year: "Agustus 2022 - September 2022",
          job: "Freelance Frontend Developer",
          company: "PT. Fazztech",
          description: ["Berpartisipasi Redesign CMS Digiexpert Telkom."]
        },
        {
          year: "Agustus 2020 - Oktober 2020",
          job: "Freelance Frontend Web Developer",
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
          job: "Freelance Frontend Web Developer",
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
