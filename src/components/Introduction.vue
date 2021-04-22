<template>
  <div class="introduction mt-3">
    <span class="py-3">
      Perkenalkan nama saya <span class="title">Keva Damar Galih</span> dan saya
      seorang Web Developer.
    </span>

    <p class="py-3">
      Saya telah bekerja di sektor teknologi informasi selama kurang lebih satu
      tahun. Dalam waktu ini, saya telah mengembangkan pengetahuan kerja tentang
      semua tren dan teknik terbaru untuk aplikasi terbaik. Saya telah bekerja
      di lingkungan komersial seperti bank dan pemerintahan. Saya juga menyukai
      tantangan dan hal baru, serta menerima project pembuatan aplikasi berbasis
      web sesuai dengan permintaan client.
    </p>

    <div class="my-3 pb-4">
      <span>Terima Kasih.</span>
      <v-icon>mdi-emoticon-cool-outline</v-icon>
    </div>
  </div>
</template>
<style>
.introduction {
  width: 90%;
  margin: auto;
}

.star {
  position: relative;
  animation: star 3s ease-in infinite;
}

@keyframes star {
  0% {
    bottom: 0;
  }
  50% {
    bottom: 5px;
    left: 4px;
  }
  100% {
    bottom: 10px;
  }
}
</style>
