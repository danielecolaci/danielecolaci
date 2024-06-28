<script setup>

</script>

<template>
  <div class="container">
    <div class="flex content">
      <div class="box"></div>
      <section class="title">
        <h1>Hi, I Am <br><span class="name">Daniele Colaci</span></h1>
      </section>
      <div class="icon flex">
        <a href="https://www.linkedin.com/in/danielecolaci/" target="_blank"><i class="fa-brands fa-linkedin"></i></a>
        <a href="https://github.com/danielecolaci" target="_blank"><i class="fa-brands fa-square-github"></i></a>
      </div>
    </div>
  </div>
</template>

<style scoped>
.box {
  width: 400px;
  height: fit-content;
  aspect-ratio: 1;
  background: url(./assets/img/dani.png) 100% center / cover;
  animation: radius 8s linear infinite;
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
  gap: 20px;
}

.title {
  text-align: center;
  font-size: 40px;
  color: white;
}


.name {
  color: blueviolet;
}

.icon {
  gap: 20px;
  font-size: 32px;
}

.fa-brands {
  color: rgb(151, 151, 151);
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

@media screen and (max-width: 768px) {
  .box {
    width: 200px;
  }

  .title {
    font-size: 20px;
  }
}
</style>
