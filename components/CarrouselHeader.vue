<template>
    <div class="relative w-full" data-carousel="slide">
        <div class="relative h-[650px] overflow-hidden md:h-[600px]">
            <!-- Div contenant le texte fixe sur le dessus avec un z-index supérieur -->
            <div class="absolute text-white top-1/4 ml-28  z-30">
                <h2 class="text-[38px] font-bold">DGL, votre partenaire en import-export</h2>
                <h3 class="text-[14px] pt-[22px]">Par <span class="text-dgl-primary">E-GBAVOU</span> | 04/09/2023 </h3>
                <p class="mt-4 text-[20px] mr-[550px]">DGL est un pionnier dans la création et la livraison de solutions
                    révolutionnaires
                    dans les secteurs de la gestion de flotte. dans les secteurs de la gestion de flotte</p>
                <AppBoutons class="mt-6">
                    Contactez-nous
                </AppBoutons>
            </div>
            <!-- Carousel wrapper en arrière-plan -->
            <div class="absolute top-0 left-0 w-full h-full z-10">
                <!-- Slide 1 -->
                <div class="hidden duration-1000 ease-in-out" :class="{ 'block': currentSlide === 0 }" data-carousel-item>
                    <img src="./../public/slideHeroHeader0.svg"
                        class="absolute block w-full -translate-x-1/2 -translate-y-1/2 top-1/2 left-1/2" alt="...">
                </div>
                <!-- Slide 2 -->
                <div class="hidden duration-1000 ease-in-out" :class="{ 'block': currentSlide === 1 }" data-carousel-item>
                    <img src="./../public/slideHeroHeader2.svg"
                        class="absolute block w-full -translate-x-1/2 -translate-y-1/2 top-1/2 left-1/2" alt="...">

                </div>
                <!-- Slide 3 -->
                <div class="hidden duration-1000 ease-in-out" :class="{ 'block': currentSlide === 2 }" data-carousel-item>
                    <img src="./../public/slideHeroHeader3.svg"
                        class="absolute block w-full -translate-x-1/2 -translate-y-1/2 top-1/2 left-1/2" alt="...">
                </div>
                <div class="hidden duration-1000 ease-in-out" :class="{ 'block': currentSlide === 3 }" data-carousel-item>
                    <img src="./../public/slideHeroHeader1.svg"
                        class="absolute block w-full -translate-x-1/2 -translate-y-1/2 top-1/2 left-1/2" alt="...">
                </div>
                <div class="hidden duration-1000 ease-in-out" :class="{ 'block': currentSlide === 4 }" data-carousel-item>
                    <img src="./../public/slideHeroHeader3.svg"
                        class="absolute block w-full -translate-x-1/2 -translate-y-1/2 top-1/2 left-1/2" alt="...">
                </div>
            </div>
        </div>

    </div>
</template>

<script setup>
import { ref } from 'vue';

const currentSlide = ref(0);

</script>
