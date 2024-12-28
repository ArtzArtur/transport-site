<script setup>
defineProps({
  imageSource: {
    type: String,
    default: ''
  }
});
const emit = defineEmits([
  'closeLightbox'
])
const closeLightbox = () => {
  emit('closeLightbox')
}
</script>

<template>
  <div class="lightbox">
    <span
    @click="closeLightbox"
    class="lightbox-close-icon">&times;</span>
    <img class="lightbox-image" :src="imageSource" alt="lightbox-image">
  </div>
</template>
