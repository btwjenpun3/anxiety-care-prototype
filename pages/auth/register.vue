<template>
    <div class="flex flex-col min-h-screen bg-[#0099e5] max-w-[430px] mx-auto">
        <div class="bg-[#0099e5] text-white p-6 pt-10 pb-12 rounded-b-3xl relative overflow-hidden">
            <h1 class="text-xl font-bold mb-1 relative z-10">Selamat Datang</h1>
            <p class="text-sm relative z-10">
                Sudah punya akun? <NuxtLink to="/auth/login" class="underline">Klik disini</NuxtLink>
            </p>

            <!-- Decorative elements -->
            <div class="absolute right-0 bottom-0 w-40 h-32 z-0">
                <div class="absolute bottom-0 right-4 flex">
                    <div class="relative">
                        <img src="https://placehold.co/600x400" class="w-96 h-24" />
                    </div>
                </div>
            </div>
        </div>

        <!-- Registration form -->
        <div class="flex-1 px-6 pt-8 pb-6 bg-white rounded-t-3xl">
            <form class="flex flex-col gap-4">
                <input type="text" placeholder="Nama" class="bg-gray-200 rounded-md p-4 text-gray-700 w-full">

                <input type="email" placeholder="Email" class="bg-gray-200 rounded-md p-4 text-gray-700 w-full">

                <input type="password" placeholder="Password" class="bg-gray-200 rounded-md p-4 text-gray-700 w-full">

                <NuxtLink to="/personalisation"
                    class="bg-[#0099e5] text-white rounded-md p-4 font-medium mt-2 text-center">
                    Daftar Gratis
                </NuxtLink>
            </form>

            <div class="mt-6 text-center">
                <p class="text-gray-600 mb-4">Atau login melalui :</p>

                <button
                    class="flex items-center justify-center gap-2 border border-gray-300 rounded-full py-3 px-6 w-full">
                    <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" preserveAspectRatio="xMidYMid"
                        viewBox="0 0 256 262">
                        <path fill="#4285F4"
                            d="M255.878 133.451c0-10.734-.871-18.567-2.756-26.69H130.55v48.448h71.947c-1.45 12.04-9.283 30.172-26.69 42.356l-.244 1.622 38.755 30.023 2.685.268c24.659-22.774 38.875-56.282 38.875-96.027">
                        </path>
                        <path fill="#34A853"
                            d="M130.55 261.1c35.248 0 64.839-11.605 86.453-31.622l-41.196-31.913c-11.024 7.688-25.82 13.055-45.257 13.055-34.523 0-63.824-22.773-74.269-54.25l-1.531.13-40.298 31.187-.527 1.465C35.393 231.798 79.49 261.1 130.55 261.1">
                        </path>
                        <path fill="#FBBC05"
                            d="M56.281 156.37c-2.756-8.123-4.351-16.827-4.351-25.82 0-8.994 1.595-17.697 4.206-25.82l-.073-1.73L15.26 71.312l-1.335.635C5.077 89.644 0 109.517 0 130.55s5.077 40.905 13.925 58.602l42.356-32.782">
                        </path>
                        <path fill="#EB4335"
                            d="M130.55 50.479c24.514 0 41.05 10.589 50.479 19.438l36.844-35.974C195.245 12.91 165.798 0 130.55 0 79.49 0 35.393 29.301 13.925 71.947l42.211 32.783c10.59-31.477 39.891-54.251 74.414-54.251">
                        </path>
                    </svg>
                    <span class="text-gray-700">Lanjutkan dengan google</span>
                </button>
            </div>
        </div>
    </div>
</template>

<script setup>
// Nuxt.js setup
</script>