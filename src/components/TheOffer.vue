<script setup>

const offers = [
  {
    title:'Dom delfinów w Marsa Alam',
    image:'/images/dolphins.jpg'
  },
  {
    title:'Codzienne wycieczki na plażę Abu Dabbab w Marsa Alam',
    image:'/images/beach-trip.jpg'
  },
  {
    title:'Super Safari',
    image:'/images/safari.jpg'
  },
]
</script>

<template>
  <section id="offer" class="offer">
    <div class="container">
    <h3 class="section-title">Oferta</h3>
    <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
      <div class="offer-card" v-for="offer in offers">
        <span class="offer-card-title">
          {{offer.title}}
        </span>
        <img class="offer-card-image" :src="offer.image" alt="dolphin-trip-image">
      </div>
    </div>
  </div>
  </section>
</template>
