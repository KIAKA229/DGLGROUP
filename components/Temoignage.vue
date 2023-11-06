<template>
    <div class="bg-blue-100 p-10 h-[650px] my-8">
        <!-- Titre -->
        <h1 class="text-center text-dgl-primary font-bold text-[26px] font-dm">Témoignages</h1>

        <!-- Sous-titre -->
        <h2 class="text-xl font-bold text-center mt-4">Ce que nos Clients Disent de Nous</h2>

        <!-- Div avec icônes précédent/suivant en SVG -->
        <div class="flex items-center justify-center mt-4 mx-[150px]">
            <img src="./../public/previous.svg" class="cursor-pointer" alt="" @click="previousTestimonial" />

            <!-- Carte contenant une image à gauche et du texte à droite -->
            <div class="grid grid-cols-2 mt-6 bg-white rounded-lg shadow-lg ">
                <!-- Image à gauche -->
                <div class="">
                    <img :src=testimonials[currentTestimonialIndex].url alt="Image du témoignage"
                        class="w-full cursor-pointer rounded-l-lg ">
                </div>

                <!-- Texte à droite -->
                <div class="p-4 py-20">
                    <p class="text-gray-600 ease-in-out transition-all duration-700">{{
                        testimonials[currentTestimonialIndex].text }}</p>

                    <div>
                        <div class="flex items-center justify-stretch pt-8 ease-in-out transition-all duration-700">
                            <!-- Image de l'utilisateur à gauche -->
                            <img src="./../public/avatar.svg" alt="Photo de profil" class="w-12 h-12 rounded-full">

                            <div class="ml-4">
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

            <img src="./../public/next.svg" class="cursor-pointer" alt="" @click="nextTestimonial" />
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue';

const currentTestimonialIndex = ref(0);
const testimonials = ref([
    {
        text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit,   sed do eiusmod tempor incididunt ut labore et dolore magna  aliqua ut enim ad minim veniam, quis nostrud  magna aliqua ut enim ad minim veniam, quis nostrud ",
        author: "Esther AHOSSI",
        position: "DEV Mobile",
        url: 'videos.svg'
    },
    {
        text: "Notre équipe expérimentée et notre réseau de livraison efficace garantissent que vos colis arrivent à destination en toute sécurité et dans les délais convenus. Que ce soit pour des livraisons locales ou internationales, ",
        author: "AKISSA Jack",
        position: "Dev web",
        url: 'video.svg'
    },
    {
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