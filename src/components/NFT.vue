<template>
    <section class="text-white px-8 sm:px-14 lg:px-20 py-20 border-b-8 border-secondary">
      <div :class="['flex','flex-col', directionClass, 'gap-8', 'md:gap-24', 'items-center']">
        <div class="basis-1/2 content sm:text-xl md:text-2xl text-xl lg:text-3xl">
          <p>
            {{ data.title }}
          </p>
          <p>
            {{ data.content }}
          </p>
          <p class="font-bold">{{ data.price }}</p>
          <a class="mt-5 block" :href="data.link">
            <svg class="border-2 border-primary rounded-full p-2" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="50" height="50">
              <path d="M9 6l6 6-6 6" fill="none" stroke="#52057B" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
            </svg>
          </a>
        </div>
        <div class="basis-1/2">
          <img class=" border-4 border-primary" :src="data.imageSrc" width="561px" :alt="data.imageAlt">
        </div>
      </div>
    </section>
</template>
  
  <script>
  import { computed } from 'vue';
  
  export default {
    name: 'ModdyCharacterNFT',
    props: {
      data: {
        type: Object,
        required: true
      }
    },
    setup(props) {
      const directionClass = computed(() => {
        return props.data.direction === 'row' ? 'sm:flex-row' : 'sm:flex-row-reverse flex-col-reverse';
      });
  
      return {
        directionClass
      };
    }
  }
  </script>
  
  <style scoped>
  img {
    max-height: 562px;
    border-radius: 0 32px 0 32px;
  }
  .content {
    max-width: 562px;
    max-height: 287px;
    margin: auto;
    line-height: 3rem;
  }
  @media screen and (max-width: 768px) {
    .content {
      line-height: 2rem;
    }
  }
  @media screen and (max-width: 640px) {
    .content {
      line-height: 2rem;
    }
  }
  </style>
  