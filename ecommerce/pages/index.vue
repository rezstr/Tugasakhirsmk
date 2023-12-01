<template>
  <div class="landing-page">
    <header class="text-center">
      <h1 class="text-4xl font-bold mb-4">Welcome to Our Site</h1>
      <p class="text-lg">Discover amazing things here!</p>
      <nav class="mt-8 flex justify-center space-x-4">
        <nuxt-link
          to="/product"
          class="text-blue-500 hover:underline link-with-border"
          >Products</nuxt-link
        >
        <nuxt-link
          to="/contact"
          class="text-blue-500 hover:underline link-with-border"
          >Contact</nuxt-link
        >
      </nav>
    </header>
    <main>
      <section class="features">
        <div class="feature">
          <h3>Design</h3>
          <p>Menyediakan design aksesoris dengan model kekinian</p>
        </div>
        <div class="feature">
          <h3>Fast</h3>
          <p>Menyediakan kecepatan aplikasi pelayanan yang cepat</p>
        </div>
        <div class="feature">
          <h3>Easy to Use</h3>
          <p>gampang digunakan oleh beberapa orang</p>
        </div>
      </section>
    </main>
  </div>
</template>

<style scoped>
/* Styling for the landing page */
/* You can customize this based on your preferences */
.landing-page {
  font-family: Arial, sans-serif;
  text-align: center;
  padding: 20px;
}

header {
  margin-bottom: 40px;
}

.features {
  display: flex;
  justify-content: space-around;
  margin-bottom: 60px;
}

.feature {
  flex: 1;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 8px;
  margin: 0 10px;
}

.link-with-border {
  border-bottom: 2px solid transparent;
}

.link-with-border:hover {
  border-bottom-color: #121212; /* Ganti dengan warna yang diinginkan */
}
</style>
