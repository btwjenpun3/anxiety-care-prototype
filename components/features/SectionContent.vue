<template>
    <div class="bg-[#0099e5] rounded-t-3xl pt-6 text-white">
        <h1 class="text-2xl font-bold text-center mb-3">{{ title }}</h1>
        <p class="text-center mb-8">{{ desc }}</p>

        <div class="flex justify-center gap-2 mb-8">
            <div v-for="i in 3" :key="i"
                :class="['w-2 h-2 rounded-full', i === dotIndex + 1 ? 'w-10 bg-[#7fcff5]' : 'bg-white']"></div>
        </div>

        <div class="flex justify-between items-center border-t border-white pt-4 w-full">
            <NuxtLink to="/auth/register" class="text-white font-medium ps-4 mb-3">Lewati</NuxtLink>
            <button v-if="!last" class="bg-white text-[#0099e5] px-6 py-2 rounded-full font-medium  ps-4 mb-3"
                @click.stop="$emit('next')">
                Lanjutkan
            </button>
            <NuxtLink v-else to="/auth/register"
                class="bg-white text-[#0099e5] px-6 py-2 rounded-full font-medium ps-4 mb-3">
                Lanjutkan
            </NuxtLink>
        </div>
    </div>
</template>

<script setup>
defineProps({
    title: String,
    desc: String,
    dotIndex: Number,
    last: Boolean
})
</script>