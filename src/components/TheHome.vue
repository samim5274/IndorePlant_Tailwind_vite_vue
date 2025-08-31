<template>
  <section id="home" class="relative">
    <div class="container mx-auto">

        <!-- blob 1  -->
         <div class="w-64 h-64 bg-green-700 rounded-full blur-3xl -z-10 opacity-40 absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2"></div>

         <!-- blob 2  -->
         <div class="w-64 h-64 bg-green-700 rounded-full blur-3xl -z-10 opacity-40 absolute right-0 bottom-0"></div>

        <div class="flex flex-col items-center gap-5 lg:flex-row">
            <!-- content  -->
            <div class="w-fuull space-y-5 lg:w-1/2">
                <h1>
                    <span class="text-yellow-500">Plants</span> make a <br>
                        positive 
                    <span class="text-yellow-500">impact</span> on <br>
                        your environment
                </h1>

                <p class="text-slate-300 font-family-lobster text-justify">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Corporis, odit voluptatum quos excepturi cum deleniti nesciunt ratione, et eius repudiandae rerum eos tenetur. Hic tenetur, asperiores esse saepe quisquam assumenda eum rem, iste modi voluptatem incidunt voluptatibus veritatis, nostrum repudiandae.</p>

                <div class="flex flex-col gap-2 sm:flex-row md:gap-4 lg:pt-5 xl:pt-10">
                    <button class="btn">
                        <span>Shop Now</span>
                        <i class="ri-leaf-line"></i>
                    </button>
                    <button class="btn btn_outline">
                        <span>Know More</span>
                        <i class="ri-leaf-line"></i>
                    </button>
                </div>

                <p class="text-xs font-family-lobster text-slate-300">you will get 30-days free trail.</p>

                <div class="flex items-center gap-5 text-lg lg:pt-10">
                    <i class="ri-facebook-fill text-slate-300 hover:text-yellow-500 duration-300 cursor-pointer"></i>
                    <i class="ri-twitter-x-line text-slate-300 hover:text-yellow-500 duration-300 cursor-pointer hover:rou"></i>
                    <i class="ri-instagram-line text-slate-300 hover:text-yellow-500 duration-300 cursor-pointer"></i>
                    <i class="ri-linkedin-fill text-slate-300 hover:text-yellow-500 duration-300 cursor-pointer"></i>
                </div>
            </div>

            <!-- imgage  -->

            <div class="w-full relative lg:w-1/2">
                <img src="/img/home.png" alt="Home">

                <!-- leaf -->
                 <div class="absolute -top-10 right-0 opacity-30 animation-movingY lg:top-5">
                    <i class="ri-leaf-line text-6xl text-yellow-500"></i>
                 </div>

                <!-- flower -->
                 <div class="absolute bottom-0 left-0 opacity-30 xl:bottom-12 animation-rotate">
                    <i class="ri-flower-line text-6xl text-yellow-500"></i>
                 </div>

                <!-- plant -->
                 <div class="hidden absolute -top-10 -left-5 opacity-30 lg:block animation-scaleUp lg:pt-10">
                    <i class="ri-plant-line text-6xl text-yellow-500"></i>
                 </div>
            </div>
        </div>
    </div>
  </section>
</template>

<style>

.animation-movingY {
    animation: moveY 3s linear infinite;
}

@keyframes moveY {
    0% {
        transform: translateY(0);
    }
    50% {
        transform: translateY(1rem);
    }
    100% {
        transform: translateY(0);
    }
}

.animation-rotate {
    animation: rotate 15s linear infinite;
}

@keyframes rotate {
    0% { transform: rotate(0deg); }
    100% { transform: rotate(360deg); }
}

.animation-scaleUp {
    animation: scaleUp 3s linear infinite
}

@keyframes scaleUp {
    0% { transform: scale(0.8); }
    50% { transform: scale(1.2); }
    100% { transform: scale(0.8); }
}
</style>
