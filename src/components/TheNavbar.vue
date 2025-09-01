<template>
  <header id="header" class="font-family-jost bg-green-950 fixed top-0 z-50 w-full" :class="{ 'border-b border-yellow-500 shadow-md': isScrolled }">
    <nav class="container mx-auto flex items-center justify-between h-16 sm:h-20">
      
      <div class="font-family-lobster lg:text-4xl md:text-3xl sm:text-2xl">IndorePlants.</div>

      <div 
        class="absolute top-0 min-h-[80vh] w-full bg-green-950/80 backdrop-blur-sm flex items-center justify-center 
               duration-300 overflow-hidden lg:static lg:min-h-fit lg:bg-transparent lg:w-auto"
        :class="menuOpen ? 'left-[0]' : 'left-[100%]'"
      >

        <ul class="flex flex-col items-center gap-8 lg:flex-row">
          <li><a href="#home" class="nav-link" @click="closeMenu">Home</a></li>
          <li><a href="#about" class="nav-link" @click="closeMenu">About</a></li>
          <li><a href="#popular" class="nav-link" @click="closeMenu">Popular</a></li>
          <li><a href="#review" class="nav-link" @click="closeMenu">Review</a></li>
        </ul>

        <div class="absolute bottom-0 -right-10 opacity-90 lg:hidden">
          <img src="/img/leaf-1.png" alt="Leaf_image" class="w-32">
        </div>
        <div class="absolute -top-5 -left-5 rotate-90 opacity-90 lg:hidden">
          <img src="/img/leaf-2.png" alt="Leaf_image" class="w-32">
        </div>
      </div>

      <div class="text-xl sm:text-3xl cursor-pointer z-50 lg:hidden" @click="toggleMenu">
        <i :class="menuOpen ? 'ri-close-large-line' : 'ri-menu-4-fill'"></i>
      </div>

    </nav>
  </header>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from "vue";

// state
const menuOpen = ref(false);
const isScrolled = ref(false);

// methods
const toggleMenu = () => {
  menuOpen.value = !menuOpen.value;
};

const closeMenu = () => {
  menuOpen.value = false;
};

const handleScroll = () => {
  isScrolled.value = window.scrollY >= 250;
};

onMounted(() => {
  window.addEventListener("scroll", handleScroll);
});
onUnmounted(() => {
  window.removeEventListener("scroll", handleScroll);
});

</script>

<style>

</style>
