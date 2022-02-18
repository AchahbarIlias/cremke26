<template>
<div>
  <div class="py-6 animate-moveintobottom bg-background fixed w-full top-0 left-0">
    <div class="container flex justify-between items-center mx-auto px-8 md:px-14 lg:px-24 w-full text-white">
      <div class="text-lg font-bold "><router-link :to="{ name: 'Home'}">Cremke'26</router-link></div>
      <div class="hidden md:flex space-x-12 items-center text-md">
        <router-link class="hover:text-green-500" :to="{ name: 'Bio'}">Menu</router-link>
        <router-link class="hover:text-green-500" :to="{ name: 'Bio'}">Openingsuren</router-link>
        <button type="button" class=" bg-green-400 hover:bg-transparent border border-transparent hover:border-green-300 font-bold rounded-sm text-sm p-2.5 text-center inline-flex items-center mr-2">
  <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z" clip-rule="evenodd"></path></svg>
  Contact
    </button>
      </div>
      <button v-on:click="toggleMenu" class="md:hidden flex flex-col space-y-1 w-8">
        <span class="bg-green-400 w-full h-1"></span>
        <span class="bg-green-400 w-full h-1"></span>
        <span class="bg-green-400 w-full h-1"></span>
      </button>
    </div>

  </div>
      <div v-if="showMenu" class="menu md:hidden fixed top-20 w-full space-y-4 flex flex-col bg-gray-200 items-center p-4">
        <router-link class="hover:text-green-500" :to="{ name: 'Menu'}">Menu</router-link>
        <button type="button" class=" bg-green-400 hover:bg-transparent border border-transparent hover:border-green-300 font-bold rounded-sm text-sm p-2.5 text-center inline-flex items-center mr-2">
  <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z" clip-rule="evenodd"></path></svg>
  Contact Me
    </button>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      showMenu: false,
    };
  },

  methods: {
    toggleMenu() {
      this.showMenu = !this.showMenu;
    },
  },
};
</script>