<template>
    <div class="flex flex-col min-h-screen bg-[#0099e5] max-w-[430px] mx-auto">
        <div class="bg-[#0099e5] text-white p-6 pt-10 pb-12 rounded-b-3xl relative overflow-hidden">
            <h1 class="text-3xl font-bold mb-1 relative z-10">Personalisasi</h1>

            <!-- Decorative elements -->
            <div class="absolute right-0 bottom-0 w-40 h-32 z-0">
                <div class="absolute bottom-0 right-4 flex">
                    <div class="relative">
                        <img src="https://placehold.co/600x400" class="w-96 h-24" />
                    </div>
                </div>
            </div>
        </div>

        <!-- Section 1 -->
        <div ref="section1" v-if="section1" class="flex-1 px-6 pt-8 pb-6 bg-white rounded-t-3xl">
            <div class="flex justify-center gap-2 mb-8">
                <div class="w-10 h-4 bg-[#7fcff5] rounded-full"></div>
                <div class="w-4 h-4 bg-gray-500 rounded-full"></div>
                <div class="w-4 h-4 bg-gray-500 rounded-full"></div>
            </div>

            <div class="">
                <div class="">
                    <h3 class="text-2xl text-center font-bold">
                        Apa Harapanmu Dengan Anxiety Care Indonesia ?
                    </h3>
                </div>
                <div class="mt-12">
                    <p class="text-center">Hal ini membantu kami untuk membuat pengalaman yang unik hanya untukmu</p>
                </div>
                <div class="mt-12">
                    <div class="flex flex-col gap-3">
                        <div class="rounded-3xl border border-[#0099e5] p-3">
                            <p class="text-center">Mendapatkan metode terapi kecemasan</p>
                        </div>
                        <div class="rounded-3xl border border-[#0099e5] p-3">
                            <p class="text-center">Mendapatkan panduan profesional</p>
                        </div>
                        <div class="rounded-3xl border border-[#0099e5] p-3">
                            <p class="text-center">Belajar mengelola kecemasan</p>
                        </div>
                        <div class="rounded-3xl border border-[#0099e5] p-3">
                            <p class="text-center">Mendapatkan dukungan komunitas</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div v-if="section1" class="absolute bottom-13 border-t-2 border-t-[#0099e5] w-[410px] sm:w-[427px] px-6 pt-12">
            <div class="flex justify-between items-center gap-2">
                <div class="">
                    <NuxtLink to="/welcome">
                        Lewati
                    </NuxtLink>
                </div>
                <div class="">
                    <button class="bg-[#0099e5] text-white rounded-3xl p-3 font-medium mt-2 text-center cursor-pointer"
                        @click="section2 = true; section1 = false">
                        Selanjutnya
                    </button>
                </div>
            </div>
        </div>

        <!-- Section 2 -->
        <div ref="section2" v-if="section2" class="flex-1 px-6 pt-8 pb-6 bg-white rounded-t-3xl">
            <div class="flex justify-center gap-2 mb-8">
                <div class="w-4 h-4 bg-gray-500 rounded-full"></div>
                <div class="w-10 h-4 bg-[#7fcff5] rounded-full"></div>
                <div class="w-4 h-4 bg-gray-500 rounded-full"></div>
            </div>

            <div class="">
                <div class="">
                    <h3 class="text-2xl text-center font-bold">
                        Jenis Konten Apa yang Menarik Untukmu ?
                    </h3>
                </div>
                <div class="mt-12">
                    <p class="text-center">
                        Beritahu preferensi kamu dalam memilih jenis konten untuk mengatasi kecemasan
                    </p>
                </div>
                <div class="mt-12">
                    <div class="flex flex-wrap gap-3">
                        <div class="rounded-3xl border border-[#0099e5] p-3">
                            <p class="text-center">Atasi stres</p>
                        </div>
                        <div class="rounded-3xl border border-[#0099e5] p-3">
                            <p class="text-center">Sensasi Gerd</p>
                        </div>
                        <div class="rounded-3xl border border-[#0099e5] p-3">
                            <p class="text-center">Cara sembuh Gerd dan Anxiety</p>
                        </div>
                        <div class="rounded-3xl border border-[#0099e5] p-3">
                            <p class="text-center">Sensasi Anxiety</p>
                        </div>
                        <div class="rounded-3xl border border-[#0099e5] p-3">
                            <p class="text-center">Cara sembuh Gerd</p>
                        </div>
                        <div class="rounded-3xl border border-[#0099e5] p-3">
                            <p class="text-center">Cara atasi gejala Anxiety</p>
                        </div>
                        <div class="rounded-3xl border border-[#0099e5] p-3">
                            <p class="text-center">Cara atasi gejala Gerd</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div v-if="section2" class="absolute bottom-13 border-t-2 border-t-[#0099e5] w-[410px] sm:w-[427px] px-6 pt-12">
            <div class="flex justify-between items-center gap-2">
                <div class="">
                    <NuxtLink to="/welcome">
                        Lewati
                    </NuxtLink>
                </div>
                <div class="">
                    <button class="bg-[#0099e5] text-white rounded-3xl p-3 font-medium mt-2 text-center  cursor-pointer"
                        @click="section3 = true; section2 = false">
                        Selanjutnya
                    </button>
                </div>
            </div>
        </div>

        <!-- Section 3 -->
        <div ref="section3" v-if="section3" class="flex-1 px-6 pt-8 pb-6 bg-white rounded-t-3xl">
            <div class="flex justify-center gap-2 mb-8">
                <div class="w-4 h-4 bg-gray-500 rounded-full"></div>
                <div class="w-4 h-4 bg-gray-500 rounded-full"></div>
                <div class="w-10 h-4 bg-[#7fcff5] rounded-full"></div>
            </div>

            <div class="">
                <div class="">
                    <h3 class="text-2xl text-center font-bold">
                        Bagaimana Cara Kamu Mengakses Metode Terapi ?
                    </h3>
                </div>
                <div class="mt-12">
                    <p class="text-center">
                        Beritahu preferensi kamu dalam memilih metode terapi untuk mengatasi kecemasan
                    </p>
                </div>
                <div class="mt-12">
                    <div class="flex flex-col gap-3">
                        <div class="rounded-3xl border border-[#0099e5] p-3">
                            <p class="text-center">Video Terapi</p>
                        </div>
                        <div class="rounded-3xl border border-[#0099e5] p-3">
                            <p class="text-center">Mengikuti Pelatihan Online</p>
                        </div>
                        <div class="rounded-3xl border border-[#0099e5] p-3">
                            <p class="text-center">Mendengarkan Audio</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div v-if="section3" class="absolute bottom-13 border-t-2 border-t-[#0099e5] w-[410px] sm:w-[427px] px-6 pt-12">
            <div class="flex justify-between items-center gap-2">
                <div class="">
                    <NuxtLink to="/welcome">
                        Lewati
                    </NuxtLink>
                </div>
                <div class="">
                    <NuxtLink to="/welcome" class="text-[#0099e5] font-medium">
                        <button
                            class="bg-[#0099e5] text-white rounded-3xl p-3 font-medium mt-2 text-center cursor-pointer">
                            Selanjutnya
                        </button>
                    </NuxtLink>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
const section1 = ref(true)
const section2 = ref(false)
const section3 = ref(false)
</script>