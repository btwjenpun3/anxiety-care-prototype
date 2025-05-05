<template>
    <div class="flex justify-center items-center min-h-screen">
        <NuxtLink to="/step">
            <FeaturesLogo />
        </NuxtLink>
    </div>
</template>

<script setup>
const router = useRouter();

onMounted(() => {
    setTimeout(() => {
        router.push('/step');
    }, 2000);
});
</script>