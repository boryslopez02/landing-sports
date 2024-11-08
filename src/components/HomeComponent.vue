<script setup>
  import { createApp, ref } from 'vue';

  let products = ref([
    {
      id: 1,
      title: 'Camiseta MLB Team A',
      team: 'MLB',
      img: '/assets/img/FV1.jpg',
      secondImg: '/assets/img/FV1-1.jpg',
      price: '$15',
      shop: 1,
    },
    {
      id: 2,
      title: 'Camiseta MLB San Diego',
      team: 'MLB',
      img: '/assets/img/FV2.jpg',
      secondImg: '/assets/img/FV2-1.jpg',
      price: '$15',
      shop: 2,
    },
    {
      id: 3,
      title: 'Camiseta MLB Chicago',
      team: 'MLB',
      img: '/assets/img/FV3.jpg',
      secondImg: '/assets/img/FV3-1.jpg',
      price: '$15',
      shop: 1,
    },
    {
      id: 4,
      title: 'Camiseta NBA Team D',
      team: 'MLB',
      img: '/assets/img/FV4.jpg',
      secondImg: '/assets/img/FV4-1.jpg',
      price: '$15',
      shop: 2,
    },
    {
      id: 5,
      title: 'Camiseta MLB Team E',
      team: 'MLB',
      img: '/assets/img/FV5.jpg',
      secondImg: '/assets/img/FV5-1.jpg',
      price: '$15',
      shop: 1,
    },
    {
      id: 6,
      title: 'Camiseta NBA Team F',
      team: 'MLB',
      img: '/assets/img/FV6.jpg',
      secondImg: '/assets/img/FV6-1.jpg',
      price: '$15',
      shop: 2,
    }
  ]);
</script>

<template>
  <div id="main">
    <div class="hero">

      <h3 class="float-text lato-black">NBA</h3>
      <h3 class="float-text lato-black">MLB</h3>

      <h1 class="main-title anton-regular">Para los <span class="text-blue">amantes</span> del <span class="badge-danger  ">deporte</span></h1>

      <!-- <img src="/assets/img/MLB.png" class="logo-mlb">
      <img src="/assets/img/NBA.png" class="logo-nba"> -->

      <div class="glass-hero"></div>
      <img src="/assets/img/bg-hero.jpg" alt="" class="bg-hero">
    </div>
  
    <div class="product-grid">
      <div class="filters">
        <p class="lato-regular">Equipos disponibles (6)</p>
        <div class="teams">
          <label for="" class="anton-regular">Miami (3)</label>
          <label for="" class="anton-regular">LA (1)</label>
          <label for="" class="anton-regular">Dodgers (4)</label>
          <label for="" class="anton-regular">Yankees (6)</label>
        </div>
      </div>
      <div class="products">
        <div 
          v-for="product in products" 
          :key="product.id" 
          class="product-card"
        >
          <div class="product-image">
            <img 
              class="main-image"
              :src="product.img" 
              :alt="product.title" 
            >
            <div class="second-image">
              <img 
                :src="product.secondImg" 
                :alt="product.title"
              >
            </div>
          </div>
          <div class="product-info">
            <p class="product-team varsity-bold text-danger">{{ product.team }}</p>
            <h2 class="product-title lato-regular">{{ product.title }}</h2>
            <p class="product-price varsity-bold">{{ product.price }}</p>
            
            <a 
              href="https://wa.me/584122958804" 
              target="_blank" 
              class="buy-button lato-black"
            >Comprar $</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped></style>