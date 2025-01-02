<template>
  <div class="container">
    <h2 class="title">Fasilitas Sekolah</h2>
    <div class="facilities-grid">
      <div 
        v-for="fasilitas in fasilitas" 
        :key="fasilitas.id" 
        class="card"
      >
        <img 
          :src="fasilitas.image" 
          :alt="fasilitas.alt" 
          class="image"
          @error="handleImageError"
        >
        <div class="overlay">
          <div class="text">{{ fasilitas.name }}</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
useHead({
  title: 'Fasilitas - SMK Negeri 4 Tasikmalaya',
  meta: [
    {
      name: 'description',
      content: 'Fasilitas Sekolah di SMK Negeri 4 Tasikmalaya',
    },
  ],
});

import kantinImg from '@/assets/img/tempat/kantin.jpeg'
import lapanganImg from '@/assets/img/tempat/lpang.jpeg'
import mesjidImg from '@/assets/img/tempat/mesjid.jpeg'
import perpusImg from '@/assets/img/tempat/perpus.jpeg'
import seniImg from '@/assets/img/tempat/seni1.jpeg'

export default {
  name: 'FasilitasSekolah',
  data() {
    return {
      fasilitas: [
        {
          id: 1,
          name: 'Kantin',
          image: kantinImg,
          alt: 'kantin'
        },
        {
          id: 2,
          name: 'Lapangan',
          image: lapanganImg,
          alt: 'lpang'
        },
        {
          id: 3,
          name: 'Mesjid',
          image: mesjidImg,
          alt: 'mesjid'
        },
        {
          id: 4,
          name: 'Perpustakaan',
          image: perpusImg,
          alt: 'perpus'
        },
        {
          id: 5,
          name: 'Ruang Seni',
          image: seniImg,
          alt: 'seni'
        }
      ]
    }
  },
  methods: {
    handleImageError(event) {
      event.target.src = kantinImg
    }
  }
}
</script>


<style scoped>
.container {
  padding: 2rem;
}

.title {
  text-align: center;
  font-size: 2rem;
  font-weight: bold;
  color: #333;
  margin-bottom: 2rem;
  margin-top: 7rem;
}

.facilities-grid {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
  justify-content: center;
}

.card {
  position: relative;
  width: 300px;
  height: 200px;
  overflow: hidden;
  border-radius: 12px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.card:hover {
  transform: translateY(-5px);
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.2);
}

.image {
  width: 100%;
  height: 100%;
  object-fit: cover;
  border-radius: 12px;
}

.overlay {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  background-color: rgba(0, 0, 0, 0.6);
  overflow: hidden;
  width: 100%;
  height: 0;
  transition: height 0.5s ease;
  border-radius: 12px;
}

.card:hover .overlay {
  height: 100%;
}

.text {
  color: white;
  font-size: 18px;
  font-weight: bold;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  text-align: center;
}

/* Responsive Design */
@media (max-width: 768px) {
  .card {
    width: 100%;
    max-width: 300px;
  }
  
  .title {
    font-size: 1.5rem;
    margin-top: 5rem;
  }
}
</style>