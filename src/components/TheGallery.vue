<script setup>
import { ref } from 'vue';
import TheLightbox from './TheLightbox.vue';
const imgSrcInLightbox = ref()
const showInLightbox = (image) => {
  imgSrcInLightbox.value = image
}
const closeLightbox = () =>{
  imgSrcInLightbox.value = null
}

const images = [
  '/images/gallery/gq1.jpg',
  '/images/gallery/gq2.jpg',
  '/images/gallery/gq3.jpg',
  '/images/gallery/gq4.jpg',
  '/images/gallery/gq5.jpg',
  '/images/gallery/gq6.jpg',
  '/images/gallery/gq7.jpg',
  '/images/gallery/gq8.jpg',
  '/images/gallery/gq9.jpg',
  '/images/gallery/gq10.jpg',
  '/images/gallery/gq11.jpg',
  '/images/gallery/gq12.jpg',
];
</script>


<template>
  <section id="gallery" class="gallery">
    <div class="container">
    <h3 class="section-title">Galeria</h3>
    <div class="gallery-grid">
      <img v-for="(image, index) in images" 
      @click="showInLightbox(image)"
      :key="index" :src="image" alt="gallery-image" class="gallery-item" />
    </div>
    <Transition name="fade">
      <template 
      v-if="imgSrcInLightbox"
      >
        <TheLightbox
          @close-lightbox="closeLightbox"
          :imageSource="imgSrcInLightbox"
        />
      </template>
    </Transition>
  </div>

  </section>
</template>


<style>
.fade-enter-active, .fade-leave-active {
  transition: opacity 0.5s;
}
.fade-enter-from, .fade-leave-to {
  opacity: 0;
}
.fade-enter-to, .fade-leave-from {
  opacity: 1;
}
</style>