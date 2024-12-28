<template>
  <header class="navbar">
    <div class="navbar-content">
      <div class="mr-auto font-bold font-sans">AdamTRANS</div>
      <nav :class="[menuOpen ? 'flex mobile-menu' : '']" class="menu">
        <a href="#about" class="nav-link">O mnie</a>
        <a href="#offer" class="nav-link">Oferta</a>
        <a href="#gallery" class="nav-link">Galeria</a>
        <a href="#contact" class="nav-link">Kontakt</a>
      </nav>
      <button @click="toggleMenu" class="md:hidden text-2xl">☰</button>
    </div>
  </header>
</template>

<script setup>
import { ref } from 'vue';

const menuOpen = ref(false);
const toggleMenu = () => {
  menuOpen.value = !menuOpen.value;
};
</script>
