<template>
  <div class="container">
    <h2>Visi & Misi SMK Negeri 4 Tasikmalaya</h2>
    <hr class="separator">
    <div class="visi-misi-container">
      <div class="image-container">
        <picture>
          <img src="assets/img/bg2.png" alt="Nature" class="responsive">
        </picture>
      </div>
      <div class="visi-text">
        <h3>Visi :</h3>
        <p>TERWUJUDNYA LULUSAN YANG CERDAS, AKTIF, KOMPETITIF, ADAPTIF, DAN PRODUKTIF BERLANDASKAN IMAN DAN TAKWA (CAKAP BERIMTAK)</p>
      </div>
    </div>
    <hr class="separator">
    <div class="misi">
      <h3  style="text-align: center;">Misi :</h3>
      <p>1.Menyiapkan Sumber Daya Manusia yang cerdas dan kompeten baik hardskill maupun softskill.</p>
      <p>2.Meningkatkan dan mengembangkan aktifitas serta kreatifitas seluruh warga sekolah dalam berbagai kegiatan positif.</p>
      <p>3.Mewujudkan manajemen pengelolaan yang efektif, efesien, transparan, akuntabel dan layanan prima.</p>
      <p>4.Menumbuhkan dan mengembangkan potensi dan kemampuan Sumber Daya Manusia yang berdaya saing tinggi melalui berbagai kegiatan akademik maupun non akademik.</p>
      <p>5.Menyelenggarakan berbagai program kegiatan dalam upaya meningkatkan Sumber Daya Manusia yang mampu menyesuaikan dengan perkembangan.</p>
      <p>6.Mengembangkan sarana prasarana dan lingkungan sekolah yang menyenangkan sebagai wadah menumbuhkembangkan daya kreasi dan inovasi untuk menghasilkan produk teknologi tepat guna.</p>
      <p>7.Membangun jiwa wirausaha yang handal melalui pembelajaran Teaching Factory (TEFA) dan Kelas Industri.</p>
      <p>8.Menjalin dan mengembangkan kemitraan dengan Industri dan Dunia Kerja (IDUKA) serta lembaga lainnya yang relevan.</p>
      <p>9.Menanamkan dan membudayakan sikap dan perilaku yang baik pada aktivitas di sekolah maupun dalam kehidupan sehari-hari.</p>
    </div>
  </div>
  
</template>

<script>
useHead({
  title: ' Visi_Misi - SMK Negeri 4 Tasikmalaya',
  meta: [
    {
      name: 'description',
      content: 'Visi & Misi SMK Negeri 4 Tasikmalaya',
    },
  ],
});

</script>

<style scoped>
.container {
  text-align: center;
  margin-top: 10rem;
}

h2 {
  font-size: 2rem;
  margin-bottom: 2rem;
}

.visi-misi-container {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-bottom: 2rem;  
}


.image-container {
  flex: 0 0 30%;
  margin-right: 2rem; 
  padding: 10px;
}


.responsive {
  width: 100%;
  height: auto; 
  max-width: 200px; 
}


.visi-text {
  flex: 1;
  text-align: left;
  padding: 3px;
}


.separator {
  width: 100%;
  border: 0;
  border-top: 2px solid #ddd; 
  margin: 10px 0; 
}

.misi {
  text-align: left;
  padding: 10px;
  width: 80%;
  margin: 0 auto; 
}

h3 {
  font-size: 1.5rem;
  font-weight: bold;
  margin-bottom: 1rem;
}

p {
  line-height: 1.6;
}
</style>
