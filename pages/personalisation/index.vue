<template>
    <div class="flex flex-col min-h-screen bg-[#0099e5] w-full max-w-[430px] mx-auto">
        <!-- Header -->
        <div class="bg-[#0099e5] text-white p-6 pt-10 pb-12 rounded-b-3xl relative overflow-hidden">
            <h1 class="text-2xl sm:text-3xl font-bold mb-1 relative z-10">Personalisasi</h1>

            <!-- Decorative elements -->
            <div class="absolute right-0 bottom-0 w-32 sm:w-40 h-24 sm:h-32 z-0">
                <div class="absolute bottom-0 right-2 sm:right-4 flex">
                    <div class="relative">
                        <img src="https://placehold.co/600x400" class="w-72 sm:w-96 h-16 sm:h-24" alt="Decoration" />
                    </div>
                </div>
            </div>
        </div>

        <div class="flex-1 relative bg-white">
            <!-- Section 1 -->
            <div ref="section1" v-if="section1" class="px-4 sm:px-6 pt-6 sm:pt-8 pb-6 bg-white rounded-t-3xl">
                <div class="flex justify-center gap-2 mb-6 sm:mb-8">
                    <div class="w-8 sm:w-10 h-3 sm:h-4 bg-[#7fcff5] rounded-full"></div>
                    <div class="w-3 sm:w-4 h-3 sm:h-4 bg-gray-500 rounded-full"></div>
                    <div class="w-3 sm:w-4 h-3 sm:h-4 bg-gray-500 rounded-full"></div>
                </div>

                <div class="space-y-6 sm:space-y-8">
                    <div>
                        <h3 class="text-xl sm:text-2xl text-center font-bold">
                            Apa Harapanmu Dengan Anxiety Care Indonesia?
                        </h3>
                    </div>
                    <div>
                        <p class="text-sm sm:text-base text-center">Hal ini membantu kami untuk membuat pengalaman yang
                            unik hanya untukmu</p>
                    </div>
                    <div>
                        <div class="flex flex-col gap-2 sm:gap-3">
                            <div v-for="(option, index) in section1Options" :key="index"
                                class="rounded-2xl sm:rounded-3xl border border-[#0099e5] p-2 sm:p-3 cursor-pointer hover:bg-blue-50 transition-colors"
                                @click="selectOption('section1', index)">
                                <p class="text-sm sm:text-base text-center">{{ option }}</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Section 2 -->
            <div ref="section2" v-if="section2" class="px-4 sm:px-6 pt-6 sm:pt-8 pb-6 bg-white rounded-t-3xl">
                <div class="flex justify-center gap-2 mb-6 sm:mb-8">
                    <div class="w-3 sm:w-4 h-3 sm:h-4 bg-gray-500 rounded-full"></div>
                    <div class="w-8 sm:w-10 h-3 sm:h-4 bg-[#7fcff5] rounded-full"></div>
                    <div class="w-3 sm:w-4 h-3 sm:h-4 bg-gray-500 rounded-full"></div>
                </div>

                <div class="space-y-6 sm:space-y-8">
                    <div>
                        <h3 class="text-xl sm:text-2xl text-center font-bold">
                            Jenis Konten Apa yang Menarik Untukmu?
                        </h3>
                    </div>
                    <div>
                        <p class="text-sm sm:text-base text-center">
                            Beritahu preferensi kamu dalam memilih jenis konten untuk mengatasi kecemasan
                        </p>
                    </div>
                    <div>
                        <div class="grid grid-cols-2 gap-2 sm:gap-3">
                            <div v-for="(option, index) in section2Options" :key="index"
                                class="rounded-2xl sm:rounded-3xl border border-[#0099e5] p-2 sm:p-3 cursor-pointer hover:bg-blue-50 transition-colors"
                                @click="selectOption('section2', index)">
                                <p class="text-xs sm:text-sm text-center">{{ option }}</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Section 3 -->
            <div ref="section3" v-if="section3" class="px-4 sm:px-6 pt-6 sm:pt-8 pb-6 bg-white rounded-t-3xl">
                <div class="flex justify-center gap-2 mb-6 sm:mb-8">
                    <div class="w-3 sm:w-4 h-3 sm:h-4 bg-gray-500 rounded-full"></div>
                    <div class="w-3 sm:w-4 h-3 sm:h-4 bg-gray-500 rounded-full"></div>
                    <div class="w-8 sm:w-10 h-3 sm:h-4 bg-[#7fcff5] rounded-full"></div>
                </div>

                <div class="space-y-6 sm:space-y-8">
                    <div>
                        <h3 class="text-xl sm:text-2xl text-center font-bold">
                            Bagaimana Cara Kamu Mengakses Metode Terapi?
                        </h3>
                    </div>
                    <div>
                        <p class="text-sm sm:text-base text-center">
                            Beritahu preferensi kamu dalam memilih metode terapi untuk mengatasi kecemasan
                        </p>
                    </div>
                    <div>
                        <div class="flex flex-col gap-2 sm:gap-3">
                            <div v-for="(option, index) in section3Options" :key="index"
                                class="rounded-2xl sm:rounded-3xl border border-[#0099e5] p-2 sm:p-3 cursor-pointer hover:bg-blue-50 transition-colors"
                                @click="selectOption('section3', index)">
                                <p class="text-sm sm:text-base text-center">{{ option }}</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Footer Navigation -->
        <div v-if="section1 || section2 || section3"
            class="sticky bottom-0 bg-white border-t-2 border-t-[#0099e5] w-full px-4 sm:px-6 py-4 sm:pt-6">
            <div class="flex justify-between items-center">
                <NuxtLink to="/welcome"
                    class="text-sm sm:text-base text-gray-600 hover:text-gray-800 transition-colors">
                    Lewati
                </NuxtLink>
                <button v-if="section1"
                    class="bg-[#0099e5] text-white rounded-2xl sm:rounded-3xl px-4 sm:px-6 py-2 sm:py-3 text-sm sm:text-base font-medium hover:bg-[#0088cc] transition-colors"
                    @click="nextSection">
                    Selanjutnya
                </button>
                <button v-else-if="section2"
                    class="bg-[#0099e5] text-white rounded-2xl sm:rounded-3xl px-4 sm:px-6 py-2 sm:py-3 text-sm sm:text-base font-medium hover:bg-[#0088cc] transition-colors"
                    @click="nextSection">
                    Selanjutnya
                </button>
                <NuxtLink v-else to="/welcome" class="text-sm sm:text-base">
                    <button
                        class="bg-[#0099e5] text-white rounded-2xl sm:rounded-3xl px-4 sm:px-6 py-2 sm:py-3 font-medium hover:bg-[#0088cc] transition-colors">
                        Selanjutnya
                    </button>
                </NuxtLink>
            </div>
        </div>
    </div>
</template>

<script setup>
const section1 = ref(true);
const section2 = ref(false);
const section3 = ref(false);

const section1Options = ref([
    "Mendapatkan metode terapi kecemasan",
    "Mendapatkan panduan profesional",
    "Belajar mengelola kecemasan",
    "Mendapatkan dukungan komunitas"
]);

const section2Options = ref([
    "Atasi stres",
    "Sensasi Gerd",
    "Cara sembuh Gerd dan Anxiety",
    "Sensasi Anxiety",
    "Cara sembuh Gerd",
    "Cara atasi gejala Anxiety",
    "Cara atasi gejala Gerd"
]);

const section3Options = ref([
    "Video Terapi",
    "Mengikuti Pelatihan Online",
    "Mendengarkan Audio"
]);

const selectedOptions = ref({
    section1: null,
    section2: null,
    section3: null
});

const selectOption = (section, index) => {
    selectedOptions.value[section] = index;
};

const nextSection = () => {
    if (section1.value) {
        section1.value = false;
        section2.value = true;
    } else if (section2.value) {
        section2.value = false;
        section3.value = true;
    }
};
</script>