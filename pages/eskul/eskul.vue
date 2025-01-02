<template>
  <div class="team-section container my-5">
    <div class="row g-4">
      <h2 class="section-title">Ekstrakulikuler di SMKN 4 Tasikmalaya</h2>
      <div v-for="(eskul, i) in eskul" :key="i" class="col-md-4 col-sm-6">
        <div class="logo-card text-center">
          <div class="logo-image-wrapper mb-4">
            <img  :src="eskul.foto" alt="basket" class="logo-image">
          </div>
          <h3 class="nama_eskul">{{ eskul.judul }}</h3>
          <div class="back-button">
      <nuxt-link :to="`/eskul/${eskul.id}`" class="d-flex align-items-center">
        <span class="ms-2">Selengkapnya
        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-arrow-right-circle" viewBox="0 0 16 16">
  <path fill-rule="evenodd" d="M1 8a7 7 0 1 0 14 0A7 7 0 0 0 1 8m15 0A8 8 0 1 1 0 8a8 8 0 0 1 16 0M4.5 7.5a.5.5 0 0 0 0 1h5.793l-2.147 2.146a.5.5 0 0 0 .708.708l3-3a.5.5 0 0 0 0-.708l-3-3a.5.5 0 1 0-.708.708L10.293 7.5z"/>
</svg>
</span>
      </nuxt-link>
    </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
useHead({
  title: 'Ekstrakulikuler  - SMK Negeri 4 Tasikmalaya',
  meta: [
    {
      name: 'description',
      content: 'Ekstrakulikuler di SMKN 4 Tasikmalaya',
    },
  ],
});

const supabase = useSupabaseClient();

const eskul = ref([]);

const geteskul = async () => {
  const { data, error } = await supabase
    .from("eskul")
    .select(`*`)
  
  if (data) eskul.value = data;
}

onMounted(() => {
  geteskul();

});

</script>

<style scoped>
.row{
  margin-top: 7rem;
}

.logo-card {
  background: #fff;
  padding: 30px;
  border-radius: 10px;
  box-shadow: 0 0 20px rgba(0, 0, 0, 0.1);
  transition: all 0.3s ease;
  margin-top: 7px; 
}

.logo-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 5px 25px rgba(0, 0, 0, 0.15);
}

.logo-image-wrapper {
  width: 150px;
  height: 150px;
  margin: 0 auto;
  border-radius: 50%;
  overflow: hidden;
}

.logo-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: all 0.3s ease;
}

.nama_eskul {
  color: #2c3e50;
  font-size: 1.5rem;
  margin-bottom: 0.5rem;
  font-weight: 600;
}

.section-title {
  text-align: center;
  font-size: 2rem;
  color: #333;
  font-weight: 700;
  margin-bottom: 5px; 
}

/* Responsive  */
@media (max-width: 768px) {
  .member-image-wrapper {
    width: 120px;
    height: 120px;
  }

  .nama_eskul {
    font-size: 1.3rem;
  }

  /* Mengatur agar kolom 100% lebar pada layar kecil */
  .col-sm-6 {
    flex: 0 0 100%;
  }

  .section-title {
    font-size: 2rem;
  }
}

.back-button {
  margin-bottom: 20px;
}

.back-button a {
  text-decoration: none;
  color: hsl(212, 100%, 64%);
  font-size: 16px;
}

.back-button a:hover {
  color: #65ceff;
}

</style>
