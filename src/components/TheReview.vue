<template>
  <section id="review-section" class="container mx-auto relative mb-20 md:mb-28 overflow-hidden">

    <div class="absolute -top-8 -left-12 opacity-50">
        <img src="/img/leaf-4.png" alt="Leaf img" class="w-40 md:w-52 xl:w-64">
    </div>

    <div class="flex flex-col items-center gap-3 text-center mb-10 md:mb-20">
        <h2 class="title font-family-lobster">Customer Review</h2>
        <p class="max-w-2xl">Follow instruction for more</p>
    </div>

    <div class="container">
        <div class="swiper py-12">
            <ul class="swiper-wrapper">
                <li class="swiper-slide" v-for="n in 4" :key="n">
                    <div class="flex flex-col gap-5 bg-green-900 rounded-md p-6">
                    <p class="font-family-lobster">
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Pariatur alias quidem eius illo nam ut tempora quisquam dicta!
                    </p>

                    <div class="flex items-center">
                        <img :src="`/img/review-${n}.jpg`" alt="Review Image" class="w-12 h-12 rounded-full" />

                        <div class="ml-2">
                        <p class="text-yellow-500 uppercase">John Doe</p>
                        <p>Designer</p>
                        </div>
                        <i class="ri-double-quotes-r text-4xl ml-auto"></i>
                    </div>
                    </div>
                </li>
            </ul>

            <div class="swiper-pagination"></div>
        </div>
    </div>
  </section>
</template>

<script setup>
import { onMounted } from "vue";

onMounted(() => {
  new Swiper(".swiper", {
    speed: 400,
    spaceBetween: 30,
    autoplay: {
      delay: 3000,
      disableOnInteraction: false,
    },
    pagination: {
      el: ".swiper-pagination",
      clickable: true,
    },
    grabCursor: true,
    breakpoints: {
      640: {
        slidesPerView: 1,
      },
      768: {
        slidesPerView: 2,
      },
      1024: {
        slidesPerView: 3,
      },
    },
  });
});
</script>

<style scoped>

</style>