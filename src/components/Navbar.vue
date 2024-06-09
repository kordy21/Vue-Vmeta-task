<template>
  <MenuMobile v-if="isMenuMobile" @MenuMobile="toggleMenuMobile"/>
  <nav class="navbar px-8 sm:px-14 lg:px-20 ">
    <div class="navbar-logo flex flex-row relative">
      <img class="fill-white" src="../../../public/Images/Frame 2.png" width="200" alt="Logo" />
    </div>
    <ul class="hidden md:flex">
      <li v-for="item in navbarItems" :key="item.text" class="navbar-item">
        <a :href="item.link" class="navbar-link">{{ item.text }}</a>
      </li>
    </ul>
    <div class="navbar-buttons">
      <button @click="login" class="navbar-button">Login</button>
      <button @click="signup" class="navbar-button">Sign Up</button>
    </div>
    <button @click="toggleMenuMobile" class="navbar-toggle md:hidden">
      <svg class="hover:fill-secondary-100" stroke="currentColor" fill="currentColor" stroke-width="0" viewBox="0 0 24 24" height="1em" width="1em" xmlns="http://www.w3.org/2000/svg"><g><path fill="none" d="M0 0h24v24H0z"></path><path d="M3 4h18v2H3V4zm6 7h12v2H9v-2zm-6 7h18v2H3v-2z"></path></g></svg>
    </button>
  </nav>
</template>

<script>
import { ref } from 'vue';
import MenuMobile from './MenuMobile.vue';

export default {
  components:{
    MenuMobile
  },
  emits: ['toggleDM'],
  setup(__,{ emit }) {
    const navbarItems = ref([
      { text: 'Home', link: '#home' },
      { text: 'About', link: '#about' },
      { text: 'Services', link: '#services' },
      { text: 'Contact', link: '#contact' }
    ]);

    const isMobile = ref(false);
    const isMenuMobile = ref(false);

    const login = () => {
      console.log('Login clicked');
    };

    const signup = () => {
      console.log('Sign Up clicked');
    };

    const toggleMobile = () => {
      isMobile.value = !isMobile.value;
    };
    const toggleMenuMobile = () => {
      isMenuMobile.value=!isMenuMobile.value
    };

    return {
      navbarItems,
      isMobile,
      login,
      signup,
      toggleMobile,
      isMenuMobile,
      toggleMenuMobile
    };
  }
};
</script>

<style scoped>
.navbar {
  @apply sticky top-0  flex justify-between items-center w-full bg-black bg-opacity-70 z-10 py-4;
}

.navbar-logo img {
  @apply h-10;
}

.navbar-buttons {
  @apply flex hidden md:flex;
}


.navbar-button {
  @apply bg-transparent text-xs font-thin md:text-lg md:font-normal border rounded-full border-primary  text-white md:py-2 px-4 mr-4 cursor-pointer;
}

.navbar-button:last-child{
  @apply bg-primary
}

.navbar-toggle {
  @apply bg-transparent border-none text-white cursor-pointer;
}

.navbar-items {
  @apply list-none flex;
}

.navbar-item {
  @apply mr-4;
}

.navbar-link {
  @apply text-white no-underline hover:text-primary;
}

@media (max-width: 768px) {
  .navbar ul {
    @apply hidden md:flex;
  }

  .navbar-buttons {
    @apply md:flex;
  }

  .navbar-toggle {
    @apply block;
  }
}
</style>
