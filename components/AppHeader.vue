<template>
    <header class="sticky z-50 shadow-sm shadow-green-200">
        <div class="container mx-auto flex justify-between items-center">
            <!-- Logo -->
            <div class="mx-4 md:mx-8">
                <img src="./../public/LOGO DGLGROUP-02.svg" class="h-16 md:h-20 w-24 md:w-28" />
            </div>

            <div class="md:flex hidden sm:items-center space-x-4 md:space-x-8 mr-8 md:mr-16">
                <!-- Navigation web-->
                <NuxtLink v-for="link in links" :key="link.to" :to="link.to"
                    class="text-black text-[16px] md:text-[18px] font-dm hover:text-dgl-primary ease-in-out transition-all duration-700"
                    :class="{ 'text-dgl-primary': $route.path === link.to }">
                    {{ link.text }}
                </NuxtLink>
                <AppBoutons>Contactez-vous</AppBoutons>
            </div>

            <!-- Menu Hamburger (pour les écrans mobiles) -->
            <button class="md:hidden mx-4" @click="toggleMenu">
                <img src="Menu.svg" alt="" class="cursor-pointer" />
            </button>
        </div>

        <!-- Mobile Navigation -->
        <div v-show="isMenuOpen" class="md:hidden bg-blue-100 py-10">
            <div class="grid grid-cols-1 gap-8">
                <NuxtLink v-for="link in links" :key="link.to" :to="link.to"
                    class="text-black text-center text-[18px] md:text-[18px] font-dm hover:text-dgl-primary ease-in-out transition-all duration-700"
                    :class="{ 'text-dgl-primary': $route.path === link.to }">
                    {{ link.text }}
                </NuxtLink>
                <AppBoutons class="mx-auto">Contactez-vous</AppBoutons>
            </div>
        </div>
    </header>
</template>

<script setup>
import { ref } from 'vue';

const isMenuOpen = ref(false);

const toggleMenu = () => {
    isMenuOpen.value = !isMenuOpen.value;
};

const links = [
    { to: '/', text: 'Accueil' },
    { to: '/about', text: 'A propos' },
    { to: '/services', text: 'Services' },
    { to: '/blog', text: 'Blog' },
    { to: '/produit', text: 'Produits' },
];
</script>
