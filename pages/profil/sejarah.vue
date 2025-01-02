<template>
  <div class="sejarah">
    <div class="judul">
    <h2 style="text-align: center;">
      Sejarah SMK Negeri 4 Tasikmalaya
    </h2>
    <hr class="separator">
    <p class="sejarah-paragraph animate-text">
      Sejalan dengan Program Pemerintah dibidang pendidikan Menengah Kejuruan pada saat itu yakni pemerataan akses ditambah pula dengan banyaknya keinginan masyarakat yang mengharapkan adanya SMK Negeri di daerah Kecamatan Purbaratu Kota  Tasikmalaya, terutama untuk menampung tamatan dari SLTP yang ingin melanjutkan ke SMK maka beberapa tokoh masyarakat, unsur pejabat pemerintah di Kecamatan Purbaratu Kota Tasikmalaya mengusulkan kepada pemerintah Kota Tasikmalaya dan Pemerintah Provinsi Jawa Barat, agar berdirinya SMK Negeri di Kecamatan Purbaratu Kota Tasikmalaya.

Setelah melalui perjuangan yang sangat panjang dari berbagai pihak khususnya Disdik Kota Tasikmalaya dan pihak-pihak terkait lainnya sesuai prosedur dan ketentuan yang berlaku pada waktu itu dengan mengucapkan syukur Alhamdulillah akhirnya pada tahun pelajaran 2010/2011 SMK Negeri 4 Tasikmalaya mulai berdiri, pada awalnya membuka Kompetensi Keahlian Teknik Komputer dan Jaringan dengan pendaftar peserta Didik Baru pada waktu itu berjumlah 44 orang. Pada awalnya tempat belajar menumpang di SMP Negeri 17 Kota Tasikmalaya, dan sekolah induknya adalah SMK Negeri 2 Kota Tasikmalaya, Untuk Tenaga pendidik dan Tenaga Kependidikan masih dibantu sepenuhnya oleh kedua sekolah tersebut.

Pada tahun 2012 keluarlah surat Izin Pendirian berdasarkan keputusan kepala Badan Pelayanan Perizinan Terpadu Kota Tasikmalaya No. 420/9/SK-BPPT/2012 Tanggal 06 Februari 2012.
    </p>
  </div>
  
    <div class="photo-section">
      <img src="/assets/img/bg2.png" alt="logo" class="photo" />
    </div>
  </div>
  
  </template>
  
  <script>
useHead({
  title: ' Sejarah - SMK Negeri 4 Tasikmalaya',
  meta: [
    {
      name: 'description',
      content: ' Sejarah SMK Negeri 4 Tasikmalaya ',
    },
  ],
});

</script>

  <style scoped>
  .separator {
  width: 100%;
  border: 0;
  border-top: 2px solid #ddd; 
  margin: 10px 0; 
}

   .sejarah {
    display: grid;
    grid-template-columns: 2fr 1fr; 
    gap: 20px;
    align-items: start;
    margin-top: 9rem;
  }
  
  /* Foto */
  .photo-section {
    display: flex;
    justify-content: center;
    align-items: flex-start; 
    margin-top: 9.5rem; 
  }
  
  .photo {
    width: 100%;
    max-width: 300px;
    height: auto;
    border-radius: 8px;
    object-fit: cover;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
  }
  
  .judul {
    max-width: 800px; 
    margin: 0 auto; 
    padding: 20px; 
    text-align: justify; 
  }
  
  /* Paragraf */
  .sejarah-paragraph {
    font-size: 1rem;
    line-height: 1.8;
    color: #333;
    margin: 1rem 0;
  }
  
  
  /* Animasi */
  @keyframes fadeIn {
    0% {
      opacity: 0;
      transform: translateY(20px);
    }
    100% {
      opacity: 1;
      transform: translateY(0);
    }
  }
  
  .animate-text {
    animation: fadeIn 1.5s ease-out forwards;
  }
  
 
  .sejarah-paragraph:nth-child(1) {
    animation-delay: 0.2s;
  }
  
  .sejarah-paragraph:nth-child(2) {
    animation-delay: 0.4s;
  }
  
  .welcome-paragraph:nth-child(3) {
    animation-delay: 0.6s;
  }
  
  .sejarah-paragraph:nth-child(4) {
    animation-delay: 0.8s;
  }
  
  </style>
