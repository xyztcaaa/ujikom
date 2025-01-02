<template>
  <div class="header fixed-top">
    <div class="h-img">
      <img src="~/assets/img/logo.png" alt="COVER" />
    </div>
    <div class="h-text">
      <div class="t-judul">
        <h2>SMKN 4</h2>
        <h2>TASIKMALAYA</h2>
      </div>

    
   <!-- Navbar -->
   <nav class="navbar navbar-expand-lg bg-body-tertiary">
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav me-auto mb-2 mb-lg-0">
            <!-- Beranda -->
            <li class="nav-item" :class="{ active: isActive === 'beranda' }">
              <NuxtLink to="/" class="nav-link" @click="setActive('beranda')">Beranda</NuxtLink>
            </li>
            <!-- Profil Dropdown -->
            <li class="nav-item dropdown" :class="{ active: isActive === 'profil' }">
              <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false" @click="setActive('profil')">Profil</a>
              <ul class="dropdown-menu">
                <li><NuxtLink to="/profil/sambutan" class="dropdown-item">Sambutan</NuxtLink></li>
                <li><NuxtLink to="/profil/visi_misi" class="dropdown-item">Visi Misi</NuxtLink></li>
                <li><NuxtLink to="/profil/identitas" class="dropdown-item">Identitas sekolah</NuxtLink></li>
                <li><NuxtLink to="/profil/sejarah" class="dropdown-item">Sejarah Sekolah</NuxtLink></li>
                <li><NuxtLink to="/profil/guru" class="dropdown-item">Daftar Guru</NuxtLink></li>
              </ul>
            </li>
            <!-- Kompetensi -->
            <li class="nav-item dropdown" :class="{ active: isActive === 'kompetensi' }">
              <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false" @click="setActive('kompetensi')">Kompetensi Keahlian</a>
              <ul class="dropdown-menu">
                <li><NuxtLink to="/kompetensi/pplg" class="dropdown-item">Pengembangan Perangkat Lunak dan Gim</NuxtLink></li>
                <li><NuxtLink to="/kompetensi/dkv" class="dropdown-item">Desain Komunikasi Visual</NuxtLink></li>
                <li><NuxtLink to="/kompetensi/tkj" class="dropdown-item">Teknik Jaringan Komputer dan Telekomunikasi</NuxtLink></li>
                <li><NuxtLink to="/kompetensi/toi" class="dropdown-item">Teknologi Otomasi Industri</NuxtLink></li>
                <li><NuxtLink to="/kompetensi/tbsm" class="dropdown-item">Teknik Bisnis Sepeda Motor</NuxtLink></li> 
              </ul>
            </li>
             <!-- Galeri -->
             <li class="nav-item dropdown" :class="{ active: isActive === 'galeri' }">
              <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false" @click="setActive('galeri')">Galeri</a>
              <ul class="dropdown-menu">
                <li><NuxtLink to="/galeri/fasilitas" class="dropdown-item">Fasilitas</NuxtLink></li>
                <li><NuxtLink to="/galeri/kegiatan" class="dropdown-item">Kegiatan Sekolah</NuxtLink></li>
                </ul>
            </li>
            <!-- Prestasi -->
            <li class="nav-item" :class="{ active: isActive === 'prestasi' }">
              <NuxtLink to="/prestasi/prestasi" class="nav-link" @click="setActive('prestasi')">Prestasi</NuxtLink>
            </li>
            <!-- Ekstrakurikuler -->
            <li class="nav-item" :class="{ active: isActive === 'eskul' }">
              <NuxtLink to="/eskul/eskul" class="nav-link" @click="setActive('eskul')">Ekstrakurikuler</NuxtLink>
            </li>
            <!-- Kegiatan -->
            <li class="nav-item" :class="{ active: isActive === 'kegiatan' }">
              <NuxtLink to="/seragam/seragam" class="nav-link" @click="setActive('kegiatan')">Seragam Sekolah</NuxtLink>
            </li>
          </ul>
        </div>
      </nav>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isActive: 'beranda', 
    };
  },
  methods: {
    setActive(item) {
      this.isActive = item;
    }
  }
};
</script>

<style scoped>
.header {
  display: flex;
  align-items: center;
  width: 100%;
  height: 7rem;
  background-color: #ffffff;
  color: #0485e2;
  padding: 0 10px;
  box-sizing: border-box;
  justify-content: space-between;
  border-bottom: 2px solid #8bcff1;
  box-shadow: 10px 10px 10px #cecece;
}

.h-img {
  flex-shrink: 0;
  margin-right: 30px;
  margin-left: 100px;
}

.h-img img {
  width: 95px;
  height: 95px;
  object-fit: cover;
}

.h-text {
  flex: 1;
  line-height: 1.2;
  display: flex;
  flex-direction: row;
  align-items: center;
}

.t-judul h2 {
  margin: 0;
  font-size: 30px;
  font-weight: 700;
  font-family: Inria Serif;
  text-transform: uppercase;
  padding-right: 20px;
}

.navbar {
  flex: 1;
  margin-left: 100px;
}

.navbar-nav .nav-item.active .nav-link {
  color: #7ab8ff;
  font-weight: bold;
  border-bottom: 2px solid #7ab8ff;
}

.navbar-nav .nav-item .nav-link:hover {
  color: #7b9eff;
  text-decoration: underline;
}

/* Dropdown styling */
.navbar-nav .nav-item.dropdown.active .nav-link {
  color: #7ab8ff; 
}

.navbar-nav .nav-item.dropdown-menu .dropdown-item:hover {
  background-color: #7ab8ff; 
  color: #000000; 
}
</style>