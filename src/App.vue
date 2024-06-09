<script>
import HeaderComponent from './components/HeaderComponent.vue';
import Brand from './components/Brand.vue';
import { ref } from 'vue';
import NFT from './components/NFT.vue';
import Collections from '../src/components/Collections.vue';
import Navbar from './components/Navbar.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'ParentComponent',
  components: {
    HeaderComponent,
    Brand,
    NFT,
    Collections,
    Navbar,
    Footer,
  },
  setup() {
    const ModdyCharacterData = ref({
      title :"“Moddy Character NFT”",
      content: "The image is a high-quality digital painting with a resolution of 3000x2000 pixels and is optimized for the web.",
      price: '$101,593',
      link: '#',
      imageSrc: '../public/Images/Moddy.jpeg',
      imageAlt: 'Moddy_image',
      direction: 'row' 
    });
    const KattyEfaData = ref({
      title :"“KattyEfa NFT”",
      content: "The image is a high-quality digital painting with a resolution of 5000x1250 pixels .",
      price: '$1.5 million',
      link: '#',
      imageSrc: '../public/Images/KattyEfa.jpeg',
      imageAlt: 'KattyEfa_image',
      direction: 'row-reverse' 
    });

    return {
      ModdyCharacterData,
      KattyEfaData
    };
  }
}
</script>

<template>
  <div class="bg-black">
    <Navbar />
    <HeaderComponent/>
    <Brand />
    <NFT :data="ModdyCharacterData" />
    <NFT :data="KattyEfaData" />
    <Collections />
    <Footer />
  </div>
</template>

<style>
  html, body, h1, h2, h3, h4, h5, h6, p, a, ul, ol, li, button, input, textarea {
  font-family: 'Poppins', sans-serif;
}
</style>
