<template>
    <div class="bg-[#0099e5] max-w-[430px] mx-auto min-h-[100vh] border-2 border-black/10 shadow-lg shadow-black/20">
        <slot />
    </div>
</template>


<script setup>
</script>

<style>
html,
body {
    margin: 0;
    padding: 0;
    height: 100%;
    width: 100%;
    overflow: hidden;
}

/* Force mobile-only view */
#__nuxt {
    max-width: 430px;
    margin: 0 auto;
    height: 100vh;
    overflow: hidden;
}
</style>