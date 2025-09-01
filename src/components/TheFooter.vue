<template>
    <section id="footer-section" class=" bg-yellow-200 text-green-900 pt-20 pb-10 md:pt-28 relative">
        <!-- newsletter -->
        <div class="container mx-auto text-white absolute top-0 right-0 left-0 -translate-y-1/2">
            <div class="bg-green-900 px-10 pt-5 pb-10 space-y-5 rounded-md">
                <h3><span class="text-yellow-500">Subscribe</span> to our newsletter Subscribe</h3>

                <div class="flex flex-col md:flex-row gap-3">
                    <input type="email" placeholder="Your Email Address" class="w-full px-5 py-3 text-green-900 rounded-md outline-none bg-white">
                    <button class="flex items-center justify-center gap-1 bg-green-950 px-5 py-3 rounded-md hover:opacity-80 duration-300">
                        <span>Subscribe</span>
                        <i class="ri-send-plane-2-fill"></i>
                    </button>
                </div>
            </div>
        </div>

        <!-- social icon  -->
        <div class="container mx-auto mt-16 mb-10">
            <div class="border-b border-green-500 relative">
                <div class="absolute top-0 transform -translate-y-1/2 left-0 right-0 max-w-36 mx-auto">
                    <div class=" bg-yellow-200 text-lg text-center space-x-2">
                        <i class="ri-facebook-fill hover:text-yellow-500 duration-300 cursor-pointer"></i>
                        <i class="ri-twitter-x-line hover:text-yellow-500 duration-300 cursor-pointer text-base"></i>
                        <i class="ri-instagram-line hover:text-yellow-500 duration-300 cursor-pointer"></i>
                        <i class="ri-linkedin-fill hover:text-yellow-500 duration-300 cursor-pointer"></i>
                    </div>
                </div>
            </div>
        </div>

        <!-- contact -->
        <div class="container mx-auto grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-4 text-center md:text-start">

        <!-- item 1 -->
        <div>
            <div class="text-7xl text-green-700 text-center inline-block">
                <i class="ri-leaf-fill"></i>
                <p class="font-family-lobster text-xl sm:text-2xl">IndorePlants.</p>
            </div>
        </div>

        <!-- item 2 -->
        <div>
            <p class="mb-5 font-bold text-xl">Quick Link</p>

            <div class="flex flex-col gap-1">
                <a href="#">Plants</a>
                <a href="#">Flowers</a>
                <a href="#">Gerdening</a>
                <a href="#">Seeds</a>
                <a href="#">Shipping</a>                    
            </div>
        </div>

        <!-- item 3 -->
        <div>
            <p class="mb-5 font-bold text-xl">Popular Services</p>

            <div class="flex flex-col gap-1">
                <a href="#">Tree Planting</a>
                <a href="#">Grass Cutting</a>
                <a href="#">Weeds Control</a>
                <a href="#">Project</a>               
            </div>
        </div>

        <!-- item 4 -->
        <div>
            <p class="mb-5 font-bold text-xl">Contact Us</p>

            <div class="flex flex-col gap-1">
                <a href="#">+880 1762 164 746</a>
                <a href="#">cse.shamim.cub@gmail.com</a>
                <a href="#">House # 02, Road # 11, Sector # 06, Uttara, Dhaka-1230.</a>
                <a href="#">Project</a>               
            </div>
        </div>
        </div>

        <!-- copyright -->
        <div class="container mx-auto">
            <p class="text-center mt-10 opacity-50">Copyright &copy; 2024 LightCode. All rights reserved.</p>
        </div>

        <!-- floral image -->
        <div class=" absolute bottom-0 left-0 opacity-20 pointer-events-none">
            <img src="/img/floral-1.png" alt="Floral Image" class="w-full lg:w-1/2">
        </div>

        <!-- scroll button -->
         <button
            @click="scrollToTop"
            class="fixed right-4 bg-yellow-500 shadow-lg flex items-center justify-center 
                    w-12 h-12 rounded-full text-white hover:text-green-950 opacity-50 hover:opacity-100 text-2xl z-50 
                    hover:-translate-y-1 transition duration-300"
            :class="isVisible ? 'bottom-6' : '-bottom-20'">
            <i class="ri-arrow-up-line"></i>
        </button>
    </section>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from "vue";

const isVisible = ref(false);

const handleScroll = () => {
  isVisible.value = window.scrollY >= 250;
};

const scrollToTop = () => {
  window.scrollTo({
    top: 0,
    behavior: "smooth",
  });
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