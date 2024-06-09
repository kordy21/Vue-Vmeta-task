<template>
  <header class="header">
    <div class="overlay"></div>
    <div class="header-content">
      <div class="content">
        <h1 class="">Your own NFT Market place without Coding</h1>
        <p class="">The fastest and easiest way to fully unlock the potential of your digital assets. Create and run an exclusive marketplace for your NFT business today!</p>
        <div class="mt-5">
          <input type="email" placeholder="Enter your email..... " class="px-4 py-2 bg-black rounded-xl border-0 outline-0">
          <button class="bg-primary px-4 py-2 ml-2 rounded-full border-none text-white cursor-pointer">Start Free</button>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'HeaderComponent',
});
</script>

<style scoped>
.header {
  position: relative;
  width: 100%;
  height: 150vh;
  background-image: url('../../public/Images/header.jpeg');
  background-size: cover;
  background-repeat: no-repeat;
  background-position: 0 -200px;
}
@media screen and (max-width: 640px) {
  .header{
    background-position: 0;
    height: 100vh; 
  }
}
.overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(180deg, #00000084, #000000);
}
.header-content {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
@media screen and (max-width: 992px) {
  .header-content {
    width: 80%;
  }
}
.content {
  text-align: center;
  color: white;
}
@media screen and (max-width: 640px) {
  .content h1{
    font-size: 32px;
  }
  .content p{
    font-size: 16px;
  }
}
h1 {
  margin: 0;
  font-size: 2.5rem;
}

p {
  margin: 0.5rem 0 0;
  font-size: 1.25rem;
}
</style>
