<template>
    <div class="container pt-5">
      <div class="row justify-content-center">
        <div class="col">
          <div id="carouselExampleIndicators" class="carousel slide" data-bs-ride="true">
            <div class="carousel-indicators">
              <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="0" class="active"
                aria-current="true" aria-label="Slide 1"></button>
              <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="1"
                aria-label="Slide 2"></button>
              <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="2"
                aria-label="Slide 3"></button>
            </div>
            <div class="carousel-inner rounded-5">
              <div class="carousel-item active">
                <img src="/assets/img/jurusan/toi/2.png" class="d-block w-100" alt="toi">
              </div>
              <div class="carousel-item">
                <img src="/assets/img/jurusan/toi/3.png" class="d-block w-100" alt="toi">
              </div>
              <div class="carousel-item">
                <img src="/assets/img/jurusan/toi/1.png" class="d-block w-100" alt="toi">
              </div>
            </div>
            <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleIndicators"
              data-bs-slide="prev">
              <span class="carousel-control-prev-icon rounded-5 bg-secondary" aria-hidden="true"></span>
              <span class="visually-hidden">Previous</span>
            </button>
            <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleIndicators"
              data-bs-slide="next">
              <span class="carousel-control-next-icon rounded-5 bg-secondary" aria-hidden="true"></span>
              <span class="visually-hidden">Next</span>
            </button>
          </div>
        </div>
      </div>
      </div>
      <hr class="separator1">
      <div class="judul1">
    <div class="judul">
    <h2 style="text-align: center;">
      Teknik Otomasi Industri (TOI)
    </h2>
    <p class="info-paragraph animate-text">
        Teknik Otomasi Industri (TOI)
Konsentrasi ini mendalami teknologi otomasi di industri, meliputi pemrograman PLC, robotika, dan sistem kontrol otomatis untuk meningkatkan efisiensi dan produktivitas di sektor manufaktur.</p></div>
    <div class="photo-section">
      <img src="/assets/img/logo/toi.png" alt="logo-toi" class="photo" />
    </div>
  </div>
  <hr class="separator1">
  </template>
 
  <style scoped>
.container {
  text-align: center;
  margin-top: 10rem;
}

.responsive {
  width: 100%;
  height: auto; 
  max-width: 200px;
}

  .container{
    margin-top: 7rem;
  }

  .card:hover {
    transform: scale(1.05);
    box-shadow: 4px 4px 20px #2e2e2eae !important;
  }

  .card {
    transition: all 0.2s ease-in-out;
  }

  .cover {
    width: 100%;
  }

  .separator1 {
  border: none;
  border-top: 2px dashed #63b1ff;
  margin: 2rem 0;
}

.judul1 {
    display: grid;
    grid-template-columns: 2fr 1fr; 
    gap: 20px;
    align-items: start;
    margin-top: 1rem;
  }
  
  /* Foto */
  .photo-section {
    display: flex;
    justify-content: center;
    align-items: flex-start; 
    margin-top: 2rem; 
  }
  
  .photo {
  width: 150px; 
  height: 150px; 
  border-radius: 50%; 
  object-fit: contain;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}

  .judul {
    max-width: 800px; 
    margin: 0 auto; 
    padding: 20px; 
    text-align: justify;
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
  .welcome-paragraph:nth-child(1) {
    animation-delay: 0.2s;
  }
  
  .welcome-paragraph:nth-child(2) {
    animation-delay: 0.4s;
  }
  
  .welcome-paragraph:nth-child(3) {
    animation-delay: 0.6s;
  }
  
  .welcome-paragraph:nth-child(4) {
    animation-delay: 0.8s;
  }
  </style>