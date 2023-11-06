<template>
    <div>
        <div id="default-carousel" class="relative " data-carousel="slide">
            <!-- Carousel wrapper -->
            <div class="relative h-[650px] overflow-hidden  md:h-[600px]">
                <!-- Item 1 -->
                <div class="hidden duration-1000 ease-in-out " data-carousel-item>
                    <img src="./../public/carrouselProduit1.svg" class="absolute block " alt="...">
                </div>
                <!-- Item 2 -->
                <div class="hidden duration-1000 ease-in-out" data-carousel-item>
                    <img src="./../public/carrouselProduit2.svg" class="absolute block  " alt="...">
                </div>
                <!-- Item 3 -->
                <div class="hidden duration-1000 ease-in-out" data-carousel-item>
                    <img src="./../public/carrouselProduit3.svg" class="absolute block " alt="...">
                </div>
                <!-- Item 4 -->
                <div class="hidden duration-1000 ease-in-out" data-carousel-item>
                    <img src="./../public/carrouselProduit1.svg" class="absolute block  " alt="...">
                </div>
                <!-- Item 5 -->
                <div class="hidden duration-1000 ease-in-out h-[500px]" data-carousel-item>
                    <img src="./../public/carrouselProduit2.svg" class="absolute block " alt="...">
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