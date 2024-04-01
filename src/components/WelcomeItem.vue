<template>
  <div class="navigation">
    <button class="nav-button" @click="navigate('Home')">Home</button>
    <button class="nav-button" @click="navigate('About')">About</button>
    <button class="nav-button" @click="navigate('Profile')">Profile</button>
  </div>
</template>

<script>
export default {
  methods: {
    navigate(page) {
      // Tambahkan logika navigasi sesuai kebutuhan, misalnya router-link atau menampilkan komponen
      console.log(`Navigating to ${page}`);
    }
  }
};
</script>

<style scoped>
.navigation {
  margin-top: 20px;
  margin-left: -150px;
  position: fixed;
  top: 0;
  width: 100%;
  z-index: 999; 
}

.nav-button {
  margin: 0 10px;
  padding: 8px 16px;
  font-size: 16px;
  background-color: transparent;
  border: 2px solid transparent;
  border-radius: 8px;
  color: whitesmoke;
  cursor: pointer;
  transition: all 0.3s ease;
  animation: rotateBorder 2s linear infinite;
}

.nav-button:hover {
  color: black;
  background-color: #eee;
  border-color: #ccc;
  animation: none; /* Menghentikan animasi saat tombol dihover */
}

@keyframes rotateBorder {
  0% {
    border-color: transparent #ff5733; /* Warna pertama */
  }
  50% {
    border-color: transparent #00f ; /* Warna kedua */
  }
  50% {
    border-color: aqua, transparent, aquamarine;
  }
  100%{
    border-color: azure;
  }
}
</style>
