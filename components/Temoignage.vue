<template>
    <div class="bg-blue-100 md:p-10 h-auto md:h-[650px] my-8 py-10 ">
        <!-- Titre -->
        <h1 class="text-center text-dgl-primary font-bold text-[26px] font-dm">Témoignages</h1>




        <!-- Sous-titre -->
        <h2 class="text-xl font-bold text-center mt-4 hidden sm:block">Ce que nos Clients Disent de Nous</h2>

        <!-- Div avec icônes précédent/suivant en SVG -->
        <div class="flex items-center justify-center md:mt-4 mt-1 mx-0 md:mx-[150px]">
            <img v-if="!(testimonials[currentTestimonialIndex].id === 1)" src="./../public/previousNoLast.svg"
                class="cursor-pointer" alt="" @click="previousTestimonial" />
            <img v-if="testimonials[currentTestimonialIndex].id === 1" src="./../public/previousLast.svg"
                class="cursor-pointer" alt="" @click="previousTestimonial" />

            <!-- Carte contenant une image à gauche et du texte à droite -->
            <div class="grid grid-cols-1 md:grid-cols-2 mt-6 bg-white rounded-lg shadow-lg ">

                <div
                    class="flex items-center block sm:hidden justify-center flex-col pt-8 ease-in-out transition-all duration-700">
                    <!-- Image de l'utilisateur à gauche -->
                    <img src="./../public/avatar.svg" alt="Photo de profil" class="w-20 h-20 rounded-full ">

                    <div class="md:ml-4 ml-0 text-center md:text-left">
                        <!-- Nom de l'utilisateur -->
                        <p class="text-lg font-semibold ease-in-out transition-all duration-700">{{
                            testimonials[currentTestimonialIndex].author }}</p>

                        <!-- Poste de l'utilisateur -->
                        <p class="text-sm text-gray-600 ease-in-out transition-all duration-700">{{
                            testimonials[currentTestimonialIndex].position }}</p>
                    </div>
                </div>
                <!-- Image à gauche -->
                <div class="hidden sm:block">
                    <img :src=testimonials[currentTestimonialIndex].url alt="Image du témoignage"
                        class="w-full cursor-pointer rounded-l-lg ">
                </div>

                <!-- Texte à droite -->
                <div class="p-4 md:py-20 py-8">
                    <p class="text-gray-600 ease-in-out transition-all duration-700 text-center md:text-left">{{
                        testimonials[currentTestimonialIndex].text }}</p>

                    <div>
                        <div
                            class="hidden sm:block md:flex md:items-center md:justify-stretch pt-8 ease-in-out transition-all duration-700">
                            <!-- Image de l'utilisateur à gauche -->
                            <img src="./../public/avatar.svg" alt="Photo de profil" class="w-12 h-12 rounded-full">

                            <div class="ml-4 ">
                                <!-- Nom de l'utilisateur -->
                                <p class="text-lg font-semibold ease-in-out transition-all duration-700">{{
                                    testimonials[currentTestimonialIndex].author }}</p>

                                <!-- Poste de l'utilisateur -->
                                <p class="text-sm text-gray-600 ease-in-out transition-all duration-700">{{
                                    testimonials[currentTestimonialIndex].position }}</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <img v-if="!(testimonials[currentTestimonialIndex].id === 3)" src="./../public/nextNoLast.svg"
                class="cursor-pointer" alt="" @click="nextTestimonial" />
            <img v-if="testimonials[currentTestimonialIndex].id === 3" src="./../public/nextLast.svg" class="cursor-pointer"
                alt="" @click="nextTestimonial" />

        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue';

const currentTestimonialIndex = ref(0);
const testimonials = ref([
    {
        id: 1,
        text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit,   sed do eiusmod tempor incididunt ut labore et dolore magna  aliqua ut enim ad minim veniam, quis nostrud  magna aliqua ut enim ad minim veniam, quis nostrud ",
        author: "Esther AHOSSI",
        position: "DEV Mobile",
        url: 'videos.svg'
    },
    {
        id: 2,
        text: "Notre équipe expérimentée et notre réseau de livraison efficace garantissent que vos colis arrivent à destination en toute sécurité et dans les délais convenus. Que ce soit pour des livraisons locales ou internationales, ",
        author: "AKISSA Jack",
        position: "Dev web",
        url: 'video.svg'
    },
    {
        id: 3,
        text: "garantissent que vos colis arrivent à destination en toute sécurité et dans les délais convenus. Que ce soit pour des livraisons locales ou internationales, ",
        author: "Black Jee",
        position: "Dev web",
        url: 'videos.svg'
    },
    // Ajoutez d'autres témoignages ici
]);

const currentTestimonial = computed(() => testimonials.value[currentTestimonialIndex.value]);

const previousTestimonial = () => {
    if (currentTestimonialIndex.value > 0) {
        currentTestimonialIndex.value--;
    }
};

const nextTestimonial = () => {
    if (currentTestimonialIndex.value < testimonials.value.length - 1) {
        currentTestimonialIndex.value++;
    }
};
</script>