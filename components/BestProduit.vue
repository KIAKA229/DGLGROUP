<template>
    <div
        class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-3 xl:grid-cols-3 gap-6 px-8 sm:px-8 my-8 justify-center">
        <!-- Premier élément -->
        <div class="max-w-md bg-white border border-gray-200 rounded-2xl shadow dark:bg-gray-800 dark:border-gray-700">
            <a href="#">
                <img class="rounded-lg w-full" src="./../public/BestProduit1.svg" alt="" />
            </a>
            <div class="p-4">
                <a href="#">
                    <h5 class="mb-2 text-xl sm:text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Noteworthy
                        technology acquisitions 2021</h5>
                </a>
                <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">Here are the biggest enterprise technology
                    acquisitions of 2021 so far, in reverse chronological order.</p>
            </div>
        </div>

        <!-- Deuxième élément -->
        <div class="max-w-md bg-white border border-gray-200 rounded-2xl shadow dark:bg-gray-800 dark:border-gray-700">
            <a href="#">
                <img class="rounded-lg w-full" src="./../public/BestProduit2.svg" alt="" />
            </a>
            <div class="p-4">
                <a href="#">
                    <h5 class="mb-2 text-xl sm:text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Noteworthy
                        technology acquisitions 2021</h5>
                </a>
                <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">Here are the biggest enterprise technology
                    acquisitions of 2021 so far, in reverse chronological order.</p>
            </div>
        </div>

        <!-- Troisième élément (copiez ce bloc pour plus d'éléments) -->
        <div class="max-w-md bg-white border border-gray-200 rounded-2xl shadow dark:bg-gray-800 dark:border-gray-700">
            <a href="#">
                <img class="rounded-lg w-full" src="./../public/BestProduit2 (1).svg" alt="" />
            </a>
            <div class="p-4">
                <a href="#">
                    <h5 class="mb-2 text-xl sm:text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Noteworthy
                        technology acquisitions 2021</h5>
                </a>
                <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">Here are the biggest enterprise technology
                    acquisitions of 2021 so far, in reverse chronological order.</p>
            </div>
        </div>
    </div>
</template>


<script setup>
import { onMounted } from 'vue'
import { initFlowbite } from 'flowbite'

// initialize components based on data attribute selectors
onMounted(() => {
    initFlowbite();
})

</script>

<style lang="scss" scoped></style>