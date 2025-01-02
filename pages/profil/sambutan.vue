<template>
<div class="sambutan">
  <div class="judul">
  <h2 style="text-align: center;">
      Sambutan Kepala Sekolah
    </h2>
    <hr class="separator">
  <p class="info-paragraph animate-text">
    Assalamualaikum Warahmatullahi Wabarakatuh
  </p>
  <p class="info-paragraph animate-text">
    Selamat datang di SMKN 4 Tasikmalaya. Segala puji dan syukur kita panjatkan kehadirat Allah SWT, semoga kita semua ada dalam lindungan-Nya. 
    Dan atas perkenan-Nya pula kami dapat menghadirkan website SMK Negeri 4 Tasikmalaya ini.
    Kami berharap dengan adanya website di SMK Negeri 4 Tasikmalaya ini para pengunjung dapat mengenal lebih jauh tentang sekolah kami
    sehingga dapat mempererat tali silaturrahmi antara sekolah dengan masyarakat demi kemajuan kita bersama.
    Tiada gading yang tak retak, website kami ini masih dalam proses pengembangan, masih banyak kekurangan yang harus kami perbaiki.
    Kritik dan sarannya yang membangun sangat kami harapkan untuk pengembangan ke depan.
  </p>
  <p class="info-paragraph animate-text">
    Akhirnya, saya mengucapkan terimakasih yang sebesar-besarnya kepada semua pihak yang tidak dapat disebutkan satu persatu atas bantuan dan fasilitasnya yang telah diberikan. 
    Semoga semua yang kita lakukan bermanfaat bagi masyarakat.
  </p>
  <p class="info-paragraph animate-text">
    Wassalamu'alaikum Warahmatullahi Wabarakatuh.
  </p>
</div>

  <div class="photo-section">
    <img src="/assets/img/kepsek.png" alt="Kepala Sekolah" class="photo" />
  </div>
</div>
</template>

<script>
useHead({
  title: ' Sambutan  - SMK Negeri 4 Tasikmalaya',
  meta: [
    {
      name: 'description',
      content: '  Sambutan Kepala Sekolah ',
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

 .sambutan {
  display: grid;
  grid-template-columns: 2fr 1fr; 
  gap: 20px;
  align-items: start;
  margin-top: 9.5rem;
}

/* Foto */
.photo-section {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 1rem;
}

.photo {
  width: 100%;
  max-width: 300px;
  height: auto;
  border-radius: 8px;
  object-fit: cover;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}

/* Sambutan */
.judul {
  max-width: 800px; 
  margin: 0 auto; 
  padding: 20px; 
  text-align: justify; 
}

/* Judul */
.welcome-title {
  margin: 0 0 1rem;
  font-size: 2rem;
  color: #000;
  text-align: center;
}

/* Paragraf */
.info-paragraph {
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

/* Menambahkan delay animasi pada paragraf */
.info-paragraph:nth-child(1) {
  animation-delay: 0.2s;
}

.info-paragraph:nth-child(2) {
  animation-delay: 0.4s;
}

.info-paragraph:nth-child(3) {
  animation-delay: 0.6s;
}

.info-paragraph:nth-child(4) {
  animation-delay: 0.8s;
}

</style>