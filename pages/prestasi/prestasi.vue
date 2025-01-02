<template>
  <div class="container">
    <h1 class="judul">Prestasi</h1>
    <div class="card-row">
      <div 
        v-for="lomba in prestasi" 
        :key="lomba.id" 
        class="card"
      >
        <img 
          :src="lomba.image" 
          :alt="lomba.alt" 
          class="image"
          @error="handleImageError"
        >
        <div class="overlay">
          <div class="text">{{ lomba.title }}</div>
        </div>
      </div>
    </div>
    <div class="text-center mt-4">
      <NuxtLink :to="instagramUrl">
        <button class="tombol-btn">Lihat Lainnya</button>
      </NuxtLink>
    </div>
  </div>
</template>

<script setup>
useHead({
  title: 'Prestasi - SMK Negeri 4 Tasikmalaya',
  meta: [
    {
      name: 'description',
      content: 'Prestasi dan pencapaian siswa-siswi SMK Negeri 4 Tasikmalaya dalam berbagai bidang lomba dan kompetisi',
    },
  ],
});

import lomba1Img from '@/assets/img/lomba/lomba1.jpg'
import lomba2Img from '@/assets/img/lomba/lomba2.jpg'
import lomba3Img from '@/assets/img/lomba/lmba3.jpg'
import lomba4Img from '@/assets/img/lomba/lomba4.jpg'
import lomba5Img from '@/assets/img/lomba/lomba5.jpg'
import lomba6Img from '@/assets/img/lomba/lomba6.jpg'

const prestasi = ref([
  {
    id: 1,
    image: lomba1Img,
    title: 'Kunjungan Edukasi Duta Safety Riding',
    alt: 'Lomba 1'
  },
  {
    id: 2,
    image: lomba2Img,
    title: 'Juara 2 Bidang Lomba Film Pendek & Juara 2 Bidang Lomba Kriya',
    alt: 'Lomba 2'
  },
  {
    id: 3,
    image: lomba3Img,
    title: 'Piagam Penghargaan Beasiswa dari Perimajasa PPLG',
    alt: 'Lomba 3'
  },
  {
    id: 4,
    image: lomba4Img,
    title: 'Piagam Penghargaan Beasiswa dari Perimajasa DKV',
    alt: 'Lomba 4'
  },
  {
    id: 5,
    image: lomba5Img,
    title: 'Piagam Penghargaan Beasiswa dari Perimajasa',
    alt: 'Lomba 5'
  },
  {
    id: 6,
    image: lomba6Img,
    title: 'Juara 3 Atletik (Panca Lomba) Putra O2SN SMK Tingkat Jawa Barat 2024',
    alt: 'Lomba 6'
  }
])

const instagramUrl = ref('https://www.instagram.com/smkn4tsmofficial?igsh=YWRkMTNkaW9jNXE4')

const handleImageError = (event) => {
  event.target.src = lomba1Img
}
</script>

<style scoped>
.container {
  text-align: center;
  margin-top: 7rem;
  padding: 20px;
}

.judul {
  font-size: 2rem;
  font-weight: bold;
  margin-bottom: 3rem;
  color: #333;
}

.card-row {
  display: flex;
  justify-content: center;
  gap: 30px;
  margin-top: 2rem;
  flex-wrap: wrap;
}

.card {
  position: relative;
  width: 350px;
  height: 220px;
  overflow: hidden;
  border-radius: 12px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s, box-shadow 0.3s;
}

.card:hover {
  transform: translateY(-10px);
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
}

.image {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
  border-radius: 12px;
}

.overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.6);
  display: flex;
  justify-content: center;
  align-items: center;
  opacity: 0;
  border-radius: 12px;
  transition: opacity 0.3s ease;
}

.card:hover .overlay {
  opacity: 1;
}

.text {
  color: white;
  font-size: 18px;
  text-align: center;
  font-weight: bold;
  padding: 0 20px;
}

.tombol-btn {
  display: inline-block;
  padding: 12px 24px;
  background-color: #92c7ff;
  color: white;
  font-size: 16px;
  border-radius: 4px;
  border: none;
  cursor: pointer;
  text-align: center;
  transition: all 0.3s ease;
  margin-top: 2rem;
}

.tombol-btn:hover {
  background-color: #a1ceff;
  transform: translateY(-2px);
}

.text-center {
  text-align: center;
  margin-top: 30px;
}

/* Responsive Design */
@media (max-width: 768px) {
  .card {
    width: 100%;
    max-width: 350px;
  }
  
  .judul {
    font-size: 1.5rem;
    margin-top: 5rem;
  }
}
</style>