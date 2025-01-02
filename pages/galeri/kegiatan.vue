<template>
  <div class="container">
    <h1 class="title"> Kegiatan Sekolah SMKN 4 TASIKMALAYA</h1>
    <div class="card-container">
      <div class="card">
        <img src="assets/img/kegiatan/binsik.jpg" alt="kegitan1" class="zoom-image">
        <div class="overlay">
          <div class="text">Kegiatan Binsik siswa kelas XII</div>
        </div>
      </div>

      <div class="card">
        <img src="assets/img/kegiatan/edufair.jpg" alt="kegitan2" class="zoom-image">
        <div class="overlay">
          <div class="text">Edu fair</div>
        </div>
      </div>

      <div class="card">
        <img src="assets/img/kegiatan/jumat.jpg" alt="kegitan3" class="zoom-image">
        <div class="overlay">
          <div class="text">Jumat Pagi Mengaji</div>
        </div>
      </div>

      <div class="card">
        <img src="assets/img/kegiatan/expo.jpg" alt="kegitan4" class="zoom-image">
        <div class="overlay">
          <div class="text">Expo Creanova</div>
        </div>
      </div>

      <div class="card">
        <img src="assets/img/kegiatan/upacara.jpg" alt="kegitan5" class="zoom-image">
        <div class="overlay">
          <div class="text">Upacara Bendera</div>
        </div>
      </div>

      <div class="card">
        <img src="assets/img/kegiatan/sarapan.png" alt="kegitan6" class="zoom-image">
        <div class="overlay">
          <div class="text">Sarapan Bersama</div>
        </div>
      </div>
    </div>
    <div class="text-center mt-4">
      <NuxtLink to="https://www.instagram.com/smkn4tsmofficial?igsh=YWRkMTNkaW9jNXE4">
        <button class="tombol-btn">Lihat Lainnya</button>
      </NuxtLink>
    </div>
  </div>
  
</template>

<script>
useHead({
  title: 'Kegiatan_Sekolah - SMK Negeri 4 Tasikmalaya',
  meta: [
    {
      name: 'description',
      content: 'Kegiatan Sekolah SMKN 4 TASIKMALAYA',
    },
  ],
});</script>

<style scoped>
  .container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 32px;
    margin-top: 7.5rem;
  }

  .title {
    text-align: center;
    font-size: 30px;
    font-weight: bold;
    margin-bottom: 16px;
  }

  .card-container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 32px 24px; 
    justify-content: center;
    margin-top: 1.5rem;
  }

  .card {
    position: relative;
    width: 250px;
    height: 300px; 
    border-radius: 8px;
    overflow: hidden;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease-in-out;
  }

  .card:hover {
    transform: scale(1.05);
  }

  .zoom-image {
    display: block;
    width: 100%;
    height: 100%;
    object-fit: cover; 
    transition: transform 0.3s ease-in-out;
  }

  .overlay {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background-color: #a3e8ffb3;
    overflow: hidden;
    width: 100%;
    height: 100%;
    transform: scale(0);
    transition: transform 0.3s ease-in-out;
    border-radius: 8px;
  }

  .card:hover .overlay {
    transform: scale(1);
  }

  .text {
    color: white;
    font-size: 16px; 
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    text-align: center;
    font-weight: bold;
    text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.6);
  }

  .card:hover .zoom-image {
    transform: scale(1.1);
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
    margin-top: 1.5rem;
  }

  .tombol-btn:hover {
    background-color: #a1ceff;
    transform: translateY(-2px);
  }

  .text-center {
    text-align: center;
    margin-top: 30px;
  }
</style>

