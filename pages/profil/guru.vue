<template>
  <picture>
    <img src="assets/img/guru/bg.png" alt="bg" class="responsive">
  </picture>
  
    <!-- jumlah -->
  <h2 class="judul" style="text-align: center; margin-top: 2rem;">Data Guru</h2>
  <hr class="separator">
  <div class="row">
      <div class="col">
    <div class="info-section">
      <div class="info-box">
        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-person-video" viewBox="0 0 16 16">
  <path d="M8 9.05a2.5 2.5 0 1 0 0-5 2.5 2.5 0 0 0 0 5"/>
  <path d="M2 2a2 2 0 0 0-2 2v8a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V4a2 2 0 0 0-2-2zm10.798 11c-.453-1.27-1.76-3-4.798-3-3.037 0-4.345 1.73-4.798 3H2a1 1 0 0 1-1-1V4a1 1 0 0 1 1-1h12a1 1 0 0 1 1 1v8a1 1 0 0 1-1 1z"/>
</svg>
        <h5>Total Guru / Pendidik</h5>
        <h4>82</h4>
      </div>
      <div class="info-box">
        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-person-vcard" viewBox="0 0 16 16">
  <path d="M5 8a2 2 0 1 0 0-4 2 2 0 0 0 0 4m4-2.5a.5.5 0 0 1 .5-.5h4a.5.5 0 0 1 0 1h-4a.5.5 0 0 1-.5-.5M9 8a.5.5 0 0 1 .5-.5h4a.5.5 0 0 1 0 1h-4A.5.5 0 0 1 9 8m1 2.5a.5.5 0 0 1 .5-.5h3a.5.5 0 0 1 0 1h-3a.5.5 0 0 1-.5-.5"/>
  <path d="M2 2a2 2 0 0 0-2 2v8a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V4a2 2 0 0 0-2-2zM1 4a1 1 0 0 1 1-1h12a1 1 0 0 1 1 1v8a1 1 0 0 1-1 1H8.96q.04-.245.04-.5C9 10.567 7.21 9 5 9c-2.086 0-3.8 1.398-3.984 3.181A1 1 0 0 1 1 12z"/>
</svg>
        <h5>Total Guru BP / BK</h5>
        <h4>5</h4>
      </div>
      <div class="info-box">
        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-person-rolodex" viewBox="0 0 16 16">
  <path d="M8 9.05a2.5 2.5 0 1 0 0-5 2.5 2.5 0 0 0 0 5"/>
  <path d="M1 1a1 1 0 0 0-1 1v11a1 1 0 0 0 1 1h.5a.5.5 0 0 0 .5-.5.5.5 0 0 1 1 0 .5.5 0 0 0 .5.5h9a.5.5 0 0 0 .5-.5.5.5 0 0 1 1 0 .5.5 0 0 0 .5.5h.5a1 1 0 0 0 1-1V3a1 1 0 0 0-1-1H6.707L6 1.293A1 1 0 0 0 5.293 1zm0 1h4.293L6 2.707A1 1 0 0 0 6.707 3H15v10h-.085a1.5 1.5 0 0 0-2.4-.63C11.885 11.223 10.554 10 8 10c-2.555 0-3.886 1.224-4.514 2.37a1.5 1.5 0 0 0-2.4.63H1z"/>
</svg>
        <h5>Total Staf TU</h5>
        <h4>10</h4>
      </div>
    </div>
  </div>
</div>
<hr class="separator">
          
    <!-- Card Kepala Sekolah -->
    <div class="kepsek-card">
      <img src="assets/img/guru/kepsek.png" alt="Kepala Sekolah" class="profile-image">
      <h1>Kepala Sekolah</h1>
      <p>Kurniawan, S.Pd.,M.Pd.</p>
    </div>

  <h2 style="text-align:center; margin-top: 2rem;">Data Guru / Pendidik</h2>

  <!-- Carousel Container -->
  <div class="carousel">
    <div v-for="(guru1, i) in guru" :key="i" class="card">
      <img :src="guru1.foto" alt="Guru" class="profile-image">
      <h1>{{ guru1.nama }}</h1>
      <p>{{ guru1.mapel }}</p>
    </div>
  </div>
</template>
<script setup>
useHead({
  title: 'Daftar Guru - SMK Negeri 4 Tasikmalaya',
  meta: [
    {
      name: 'description',
      content: 'Data Guru / Pendidik di SMK Negeri 4 Tasikmalaya',
    },
  ],
});

const supabase = useSupabaseClient();

const guru = ref([]);

const getguru = async () => {
  const { data, error } = await supabase
    .from("guru")
    .select(`*`)
   
  if (data) guru.value = data;
}

onMounted(() => {
  getguru();

});

</script>
<style scoped>
.responsive {
  width: 100%;
  height: auto;
  margin-top: 8rem;
  border-radius: 10px;
}
      .info-section {
  display: flex;
  justify-content: space-around;
  padding: 1rem;
}
.info-box {
  text-align: center;
}

.kepsek-card { 
  max-width: 300px; 
  text-align: center;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
  border-radius: 10px;
  overflow: hidden;
}

.kepsek-card img {
  width: 100%; 
  height: 250px; 
  object-fit: cover; 
}

.kepsek-card h1 {
  margin: 16px 0;
  font-size: 24px;
}


.carousel {
  display: flex;
  overflow-x: auto; 
  scroll-snap-type: x mandatory; 
  gap: 16px; 
  padding: 16px;
  scrollbar-width: none; 
}

.carousel::-webkit-scrollbar {
  display: none; 
}


.card {
  flex: 0 0 270px; 
  scroll-snap-align: center; 
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2); 
  border-radius: 10px; 
  text-align: center; 
  overflow: hidden;
}

.card img {
  width: 100%; 
  height: 250px; 
  object-fit: cover; 
}

h1 {
  margin: 16px 0;
  font-size: 20px;
}
</style>


