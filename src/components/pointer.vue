<template>
    <div>
      <div
        class="glow-pointer"
        :style="{ top: yPos + 'px', left: xPos + 'px' }"
        v-show="showGlow"
      ></div>

    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        xPos: 0,
        yPos: 0,
        showGlow: false
      };
    },
    mounted() {
      document.body.addEventListener('mousemove', this.moveGlow);
    },
    methods: {
      moveGlow(event) {
        this.xPos = event.clientX;
        this.yPos = event.clientY;
  
        this.showGlow = true;
  
        setTimeout(() => {
          this.showGlow = true;
        }, 0);
      }
    }
  };
  </script>
  
  <style scoped>
  /* CSS untuk elemen bercahaya pada pointer */
  .glow-pointer {
    position: fixed;
    width: 50px;
    height: 50px;
    background-color: rgba(21, 220, 255, 0.61); /* Warna dan kejelasan efek bercahaya */
    border-radius: 50%;
    pointer-events: none; /* Memastikan elemen tidak mengganggu pointer */
    z-index: 9999; /* Pastikan elemen berada di atas semua elemen lain */
    transition: opacity 0.3s, transform 0.3s; /* Efek transisi untuk kejelasan dan perubahan ukuran */
    /* Menempatkan elemen di tengah */
    transform: translate(-50%, -50%);
  }
  
  </style>
  