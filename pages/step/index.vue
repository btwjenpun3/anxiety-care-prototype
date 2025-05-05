<template>
    <div class="flex flex-col min-h-screen bg-white">
        <!-- Logo -->
        <FeaturesLogo />

        <!-- Illustration -->
        <div class="flex justify-center items-center px-6 max-h-[45vh]">
            <img src="https://placehold.co/600x400" class="max-w-full max-h-[45vh]" />
        </div>

        <!-- Sections -->
        <div class="flex-grow flex flex-col justify-end">
            <Transition name="fade" mode="out-in">
                <div v-if="section1" key="section1" class="section">
                    <FeaturesSectionContent title="Selamat datang di Anxiety Care Indonesia !"
                        desc="Kami hadir untuk mendukung kamu dalam perjalanan menuju kesehatan mental lebih baik"
                        :dotIndex="0" @next="nextSection" />
                </div>
                <div v-else-if="section2" key="section2" class="section" @click="nextSection">
                    <FeaturesSectionContent title="Dapatkan Dukungan Bersama"
                        desc="Temukan ruang aman dalam komunitas yang memahami kesehatan mental kamu" :dotIndex="1"
                        :clickable="true" @next="nextSection" />
                </div>
                <div v-else key="section3" class="section">
                    <FeaturesSectionContent title="Pilihan Metode Terapi yang Efektif"
                        desc="Temukan metode terapi yang terbukti mengatasi kecemasan" :dotIndex="2" :last="true" />
                </div>
            </Transition>
        </div>
    </div>
</template>

<script setup>
const section1 = ref(true)
const section2 = ref(false)

const nextSection = () => {
    if (section1.value) {
        section1.value = false
        section2.value = true
    } else if (section2.value) {
        section2.value = false
    }
}
</script>

<style scoped>
.fade-enter-active,
.fade-leave-active {
    transition: opacity 0.4s;
}

.fade-enter-from,
.fade-leave-to {
    opacity: 0;
}
</style>