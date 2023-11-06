<template>
    <div>
        <div id="default-carousel" class="relative" data-carousel="slide">
            <!-- Carousel wrapper -->
            <div class="relative pl-5 sm:pl-20 overflow-hidden rounded-[18px] sm:h-[350px] sm:w-[500px] md:w-[500px]">
                <!-- Item 1 -->
                <div class="hidden duration-1000 ease-in-out rounded-[18px]" data-carousel-item>
                    <img src="./../public/ModuleGPS.svg" class="absolute block px-2 sm:px-4 sm:rounded-[18px]" alt="...">
                </div>
                <!-- Item 2 -->
                <div class="hidden duration-1000 ease-in-out rounded-[18px]" data-carousel-item>
                    <img src="./../public/CoffresIntellignent.svg" class="absolute block px-2 sm:px-4 sm:rounded-[18px]"
                        alt="...">
                </div>
                <!-- Item 3 -->
                <div class="hidden duration-1000 ease-in-out rounded-[18px]" data-carousel-item>
                    <img src="./../public/ModuleGPS.svg" class="absolute block px-2 sm:px-4 sm:rounded-[18px]" alt="...">
                </div>
                <!-- Item 4 -->
                <div class="hidden duration-1000 ease-in-out rounded-[18px]" data-carousel-item>
                    <img src="./../public/CoffresIntellignent.svg" class="absolute block px-2 sm:px-4 sm:rounded-[18px]"
                        alt="...">
                </div>
                <!-- Item 5 -->
                <div class="hidden duration-1000 ease-in-out rounded-[18px]" data-carousel-item>
                    <img src="./../public/DispoPesage.svg" class="absolute block px-2 sm:px-4 sm:rounded-[18px]" alt="...">
                </div>
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
