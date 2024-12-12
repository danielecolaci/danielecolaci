<script>
document.addEventListener("DOMContentLoaded", function () {
  const loading = document.getElementById('loading');
  const container = document.querySelector('.container');

  window.addEventListener('load', function () {
    loading.style.display = 'none';
    container.style.display = 'block';
  });
});
</script>

<template>
  <main>
  <div id="loading" class="loading-overlay" role="alert" aria-live="assertive">
    <div class="loading-spinner" aria-label="Loading... Please wait."></div>
  </div>
  <div class="container" style="display: none;">
    <div class="flex content">
      <div class="box" aria-hidden="true"></div>
      <section class="title">
        <h2>
          Hi, I Am <br>
          <span class="name">Daniele Colaci</span>
        </h2>
      </section>
      <div class="icon flex">
        <a href="https://www.linkedin.com/in/danielecolaci/" target="_blank" class="link-btn flex"
          aria-label="Connect with me on LinkedIn">
          Connected to LinkedIn
          <i class="fa-brands fa-linkedin-in" aria-hidden="true"></i>
        </a>
        <a href="https://github.com/danielecolaci" target="_blank" class="link-btn flex"
          aria-label="Follow me on GitHub">
          Follow Me on GitHub
          <i class="fa-brands fa-github" aria-hidden="true"></i>
        </a>
      </div>
      <p style="color: #808080;">Website Under Construction</p>
    </div>
  </div>
    </main>
</template>

<style>
/* Loading overlay styles */
.loading-overlay {
  position: fixed;
  width: 100vw;
  height: 100vh;
  background: #202020;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 9999;
}

.loading-spinner {
  border: 8px solid #464646;
  border-top: 8px solid white;
  border-radius: 50%;
  width: 60px;
  height: 60px;
  animation: spin 1s linear infinite;
}

@keyframes spin {
  0% {
    transform: rotate(0deg);
  }

  100% {
    transform: rotate(360deg);
  }
}

.box {
  width: 400px;
  height: fit-content;
  aspect-ratio: 1;
  background: url(./assets/img/dani.webp) 100% center / cover;
  animation: radius 8s linear infinite;
  transition: box-shadow 2s ease-in-out, transform 2s ease;

  &:hover {
    box-shadow: 0px 10px 20px rgba(0, 0, 0, 0.5);
    animation-play-state: paused;
    transform: scale(1.05);
  }
}


.container {
  height: 100vh;
  width: 100vw;
  background-color: #202020;
}

.content {
  height: 100%;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 32px;
}

.title {
  text-align: center;
  color: white;

  h2 {
    font-size: 32px;
    font-weight: 200;
  }
}

.name {
  color: #d4f365;
  font-size: 40px;
  font-weight: 700;
}

.icon {
  flex-wrap: wrap;
  justify-content: center;
  margin: 0 32px;
  gap: 40px;
  font-size: 32px;
}

.link-btn {
  font-size: 16px;
  font-weight: 500;
  text-decoration: none;
  color: #DDDDDD;
  border: 2px solid #DDDDDD;
  width: 260px;
  padding: 12px 0;
  border-radius: 12px;
  justify-content: center;
  align-items: center;
  gap: 16px;
  transition: all 1s ease;

  &:hover {
    background-color: #DDDDDD;
    color: #202020;
  }
}

@keyframes radius {

  0%,
  100% {
    border-radius: 55% 45% 70% 30% / 43% 30% 70% 60%;
  }

  33% {
    border-radius: 40% 60% 40% 60% / 70% 60% 40% 30%;
  }

  66% {
    border-radius: 20% 80% 20% 80% / 50% 45% 55% 50%;
  }
}

@media screen and (max-width: 1440px) {
  .box {
    width: 300px;
  }

  .title h2 {
    font-size: 28px;
  }

  .name {
    font-size: 36px;
  }
}

@media screen and (max-width: 768px) {
  .box {
    width: 200px;
  }

  .title h2 {
    font-size: 20px;
  }

  .name {
    font-size: 28px;
  }

  p {
    font-size: 12px;
  }

  .icon {
    gap: 16px;
  }

  .link-btn {
    font-size: 12px;
    font-weight: 500;
    width: 200px;
    gap: 12px;
  }
}
</style>
