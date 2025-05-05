<template>
    <div class="flex flex-col min-h-screen bg-white">
        <!-- Logo section -->
        <FeaturesLogo />

        <!-- Illustration section -->
        <div class="flex-1 flex justify-center items-center px-6 mb-4">
            <div class="relative w-64 h-64 bg-gray-100 rounded-full flex justify-center items-center">
                <!-- Window element -->
                <div
                    class="absolute left-1/4 top-1/4 w-16 h-20 bg-gray-200 rounded-sm grid grid-cols-2 grid-rows-3 gap-0.5">
                    <div v-for="i in 6" :key="i" class="bg-white"></div>
                </div>

                <!-- Red circle -->
                <div class="absolute left-1/6 top-1/6 w-10 h-10 bg-red-400 rounded-full"></div>

                <!-- Person -->
                <div class="absolute bottom-1/4 left-1/3">
                    <div class="w-8 h-8 bg-[#333] rounded-full overflow-hidden">
                        <div class="w-full h-5 bg-[#333] absolute bottom-0"></div>
                        <div class="w-4 h-2 bg-[#fff] absolute bottom-2 left-2 rounded-full"></div>
                    </div>
                    <div class="w-16 h-20 relative">
                        <div class="w-16 h-10 bg-[#0099e5] absolute top-0 rounded-md"></div>
                        <div class="w-8 h-12 bg-[#333] absolute bottom-0 left-2 rounded-t-md"></div>
                        <div class="w-10 h-2 bg-[#333] absolute bottom-0 left-6 rounded"></div>
                        <div class="w-12 h-1.5 bg-[#0099e5] absolute top-6 left-10 rotate-[-20deg] rounded-full"></div>
                    </div>
                </div>

                <!-- Blue cloud shape -->
                <div class="absolute right-1/6 top-1/3 w-20 h-16">
                    <div class="w-16 h-12 bg-[#0099e5] rounded-full absolute top-0 right-0"></div>
                    <div class="w-10 h-8 bg-[#0099e5] rounded-full absolute bottom-0 left-0"></div>
                    <div class="w-8 h-6 bg-[#0099e5] rounded-full absolute bottom-2 right-2"></div>
                    <div class="w-6 h-10 bg-[#333] rounded-b-full absolute bottom-0 right-4"></div>
                </div>
            </div>
        </div>

        <!-- Section 1 -->
        <div ref="section1" v-if="section1" class="bg-[#0099e5] text-white rounded-t-3xl pt-6 pb-8 px-6 h-80">
            <h1 class="text-2xl font-bold text-center mb-3">
                Selamat datang di Anxiety Care Indonesia !
            </h1>
            <p class="text-center mb-8">
                Kami hadir untuk mendukung kamu dalam perjalanan menuju kesehatan mental lebih baik
            </p>

            <!-- Pagination dots -->
            <div class="flex justify-center gap-2 mb-8">
                <div class="w-10 h-2 bg-[#7fcff5] rounded-full"></div>
                <div class="w-2 h-2 bg-white rounded-full"></div>
                <div class="w-2 h-2 bg-white rounded-full"></div>
            </div>

            <!-- Navigation buttons -->
            <div class="flex justify-between items-center border-t-3 border-white pt-4 w-full">
                <NuxtLink to="/auth/register" class="text-white font-medium">Lewati</NuxtLink>
                <button class="bg-white text-[#0099e5] px-6 py-2 rounded-full font-medium cursor-pointer"
                    @click="section1 = false; section2 = true">
                    Lanjutkan
                </button>
            </div>
        </div>

        <!-- Section 2 -->
        <div ref="section2" v-if="section2"
            class="bg-[#0099e5] text-white rounded-t-3xl pt-6 pb-8 px-6 cursor-pointer h-80"
            @click="section2 = false; section3 = true">
            <h1 class="text-2xl font-bold text-center mb-3">
                Dapatkan Dukungan Bersama
            </h1>
            <p class="text-center mb-8">
                Temukan ruang aman dalam komunitas yang memahami kesehatan mental kamu
            </p>

            <!-- Pagination dots -->
            <div class="flex justify-center gap-2 mb-8">
                <div class="w-2 h-2 bg-white rounded-full"></div>
                <div class="w-10 h-2 bg-[#7fcff5] rounded-full"></div>
                <div class="w-2 h-2 bg-white rounded-full"></div>
            </div>

            <!-- Navigation buttons -->
            <div class="flex justify-between items-center border-t-3 border-white pt-4 w-full">
                <NuxtLink to="/auth/register" class="text-white font-medium">Lewati</NuxtLink>
                <button class="bg-white text-[#0099e5] px-6 py-2 rounded-full font-medium  cursor-pointer">
                    Lanjutkan
                </button>
            </div>
        </div>

        <!-- Section 3 -->
        <div ref="section3" v-if="section3" class="bg-[#0099e5] text-white rounded-t-3xl pt-6 pb-8 px-6 h-80">
            <h1 class="text-2xl font-bold text-center mb-3">
                Pilihan Metode Terapi yang Efektif
            </h1>
            <p class="text-center mb-8">
                Temukan metode terapi yang terbukti mengatasi kecemasan
            </p>

            <!-- Pagination dots -->
            <div class="flex justify-center gap-2 mb-8">
                <div class="w-2 h-2 bg-white rounded-full"></div>
                <div class="w-2 h-2 bg-white rounded-full"></div>
                <div class="w-10 h-2 bg-[#7fcff5] rounded-full"></div>
            </div>

            <!-- Navigation buttons -->
            <div class="flex justify-between items-center border-t-3 border-white pt-4 w-full">
                <NuxtLink to="/auth/register" class="text-white font-medium">Lewati</NuxtLink>
                <NuxtLink to="auth/register"
                    class="bg-white text-[#0099e5] px-6 py-2 rounded-full font-medium cursor-pointer">
                    Lanjutkan
                </NuxtLink>
            </div>
        </div>
    </div>
</template>

<script setup>
const section1 = ref(true);
const section2 = ref(false);
const section3 = ref(false);
</script>