<template>
  <div class="introduction">
    <div class="py-3">
      Nama saya <span class="title">Keva Damar Galih</span> dan saya seorang web developer.
    </div>
    
    <div class="py-3">Saya telah bekerja di sektor teknologi informasi selama kurang lebih satu tahun. Dalam waktu ini, saya telah mengembangkan pengetahuan kerja tentang semua tren dan teknik terbaru untuk aplikasi terbaik. Saya telah bekerja di lingkungan komersial seperti bank dan pemerintahan. Saya juga ingin menjadi bagian dari tim yang terintegrasi, meskipun saya sangat mampu menangani proyek-proyek besar secara individu. Saya percaya bahwa karier ini sangat menguntungkan dan karena terus berkembang, saya berharap dapat menemukan perusahaan yang dapat berubah dengan industri itu sendiri. </div>
    
    <div class="my-3 pb-4">
      Terima Kasih. 
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
    0%{
      bottom: 0;
    }
    50%{
      bottom: 5px;
      left: 4px;
    }
    100%{
      bottom: 10px;
    }
  }
</style>