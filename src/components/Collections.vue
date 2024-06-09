<template>
  <section >
    <div class="lg:px-20 sm:px-14 px-8 py-8">
      <h1 class="text-4xl text-white font-bold">Collections</h1>
    </div>
    <!-- slider -->
    <div class="pb-20 px-2">
      <div class="flex justify-center items-center relative overflow-hidden">
        <!-- cards -->
        <div class="flex transition-transform duration-500" :style="{ transform: `translateX(-${slideOffset}px)` }">
          <!-- card -->
          <div v-for="(card, index) in cards" :key="index" class="card mx-2 relative">
            <img :src="card.image" alt="Card Image" class="rounded-xl border-2 border-primary">
            <div class="absolute text-center w-full overlay bg-black bg-opacity-75 text-white p-2 rounded-b-md">
              <p class="text-sm">{{ card.title }}</p>
              <p class="text-sm">{{ card.Floor }}</p>
            </div>
          </div>
        </div>
        <!-- buttons -->
        <div class="flex justify-between w-full absolute top-1/2 transform -translate-y-1/2">
          <button @click="slideLeft">
            <svg class="bg-primary rounded-full p-2" xmlns="http://www.w3.org/2000/svg" fill="#eee" viewBox="0 0 24 24" width="50" height="50">
              <path d="M15.41 16.59a.996.996 0 0 0 0-1.41L10.83 12l4.58-4.59a.996.996 0 1 0-1.41-1.41l-5.29 5.3a.996.996 0 0 0 0 1.41l5.29 5.29a.996.996 0 0 0 1.41 0z"/>
            </svg> 
          </button>
          <button @click="slideRight">
            <svg class="bg-primary rounded-full p-2" xmlns="http://www.w3.org/2000/svg" fill="#eee" viewBox="0 0 24 24" width="50" height="50" transform="rotate(180)">
              <path d="M15.41 16.59a.996.996 0 0 0 0-1.41L10.83 12l4.58-4.59a.996.996 0 1 0-1.41-1.41l-5.29 5.3a.996.996 0 0 0 0 1.41l5.29 5.29a.996.996 0 0 0 1.41 0z"/>
            </svg>
          </button>
        </div>
      </div>
    </div>
  </section>
</template>


<script>
import { ref, computed } from 'vue';

export default {
  setup() {
    const cards = ref([
      { image: '../public/Images/--1.jpeg', title: 'XO Girls NFT Collection', Floor: "Floor : 0.07 ETH " },
      { image: '../public/Images/2.png', title: 'Game character 3d Collection', Floor: "Floor : 0.05 ETH " },
      { image: '../public/Images/-3.jpeg', title: 'Monkey Collections', Floor: "Floor : 0.01 ETH " },
      { image: '../public/Images/-4.jpeg', title: 'PROJECT NFT cub ', Floor: "Floor : 0.07 ETH " },
      { image: '../public/Images/--1.jpeg', title: 'XO Girls NFT Collection', Floor: "Floor : 0.07 ETH " },
      { image: '../public/Images/2.png', title: 'Game character 3d Collection', Floor: "Floor : 0.05 ETH " },
      { image: '../public/Images/-3.jpeg', title: 'Monkey Collections', Floor: "Floor : 0.01 ETH " },
      { image: '../public/Images/-4.jpeg', title: 'PROJECT NFT cub ', Floor: "Floor : 0.07 ETH " },
      { image: '../public/Images/--1.jpeg', title: 'XO Girls NFT Collection', Floor: "Floor : 0.07 ETH " },
      { image: '../public/Images/2.png', title: 'Game character 3d Collection', Floor: "Floor : 0.05 ETH " },
      { image: '../public/Images/-3.jpeg', title: 'Monkey Collections', Floor: "Floor : 0.01 ETH " },
      { image: '../public/Images/-4.jpeg', title: 'PROJECT NFT cub ', Floor: "Floor : 0.07 ETH " },
    ]);
    const screenWidth = ref(window.innerWidth);
    const slideOffset = ref(0);
    const currentIndex = ref(0);

    const cardWidth = 314; 

    const visibleCardsCount = computed(() => {
      if (screenWidth.value >= 1024) {
        return 4; // Desktop
      } else if (screenWidth.value >= 768) {
        return 3; // Tablet
      } else {
        return 2; // Mobile
      }
    });

    const slideLeft = () => {
      if (currentIndex.value > 0) {
        currentIndex.value--;
      } else {
        currentIndex.value = cards.value.length - visibleCardsCount.value;
      }
      slideOffset.value = currentIndex.value * cardWidth;
    };

    const slideRight = () => {
      if (currentIndex.value < cards.value.length - visibleCardsCount.value -3) {
        currentIndex.value++;
      } else {
        currentIndex.value = 0;
      }
      slideOffset.value = currentIndex.value * cardWidth;
    };

    window.addEventListener('resize', () => {
      screenWidth.value = window.innerWidth;
    });

    return { cards, slideLeft, slideRight, slideOffset };
  }
};
</script>

<style scoped>
.card {
  width: 314px;
  transition: transform 0.5s ease-in-out;
}
.card div {
  bottom: 0;
}
</style>
