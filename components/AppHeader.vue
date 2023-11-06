<template>
    <header class="sticky z-50 shadow-sm shadow-green-200">
        <div class="container mx-auto flex justify-between items-center">
            <!-- Logo -->
            <div class="mx-8">
                <img src="./../public/LOGO DGLGROUP-02.svg" class="h-20 w-28" />
            </div>

            <div>
                <!-- Navigation -->
                <nav class="md:flex hidden sm:items-center">
                    <div class="space-x-8 mr-16">

                        <NuxtLink to="/"
                            class=" font-montserrat text-[18px] hover:text-dgl-primary ease-in-out transition-all duration-700"
                            :class="{ 'text-dgl-primary': $route.path === '/' }">
                            Accueil</NuxtLink>
                        <NuxtLink to="/about"
                            class="text-black text-[18px]  font-dm hover:text-dgl-primary ease-in-out transition-all duration-700"
                            :class="{ 'text-dgl-primary': $route.path === '/about' }">A propos
                        </NuxtLink>
                        <NuxtLink to="/services"
                            class="text-black text-[18px]  font-dm hover:text-dgl-primary transition duration-300"
                            :class="{ 'text-dgl-primary': $route.path === '/services' }">Services
                        </NuxtLink>
                        <NuxtLink to="/blog"
                            class="text-black text-[18px]  font-dm hover:text-dgl-primary transition duration-300"
                            :class="{ 'text-dgl-primary': $route.path === '/blog' }">Blog
                        </NuxtLink>
                        <NuxtLink to="/produit"
                            class="text-black text-[18px]  font-dm hover:text-dgl-primary transition duration-300"
                            :class="{ 'text-dgl-primary': $route.path === '/produit' }">Produits
                        </NuxtLink>
                    </div>
                    <AppBoutons class="mt-1">
                        Contactez-vous
                    </AppBoutons>
                </nav>
            </div>

            <!-- Menu Hamburger (pour les écrans mobiles) -->
            <button class="md:hidden mx-8">
                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor"
                    class="w-8 h-8 text-dgl-primary">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7" />
                </svg>
            </button>
        </div>
    </header>
</template>

<script setup>

</script>

<style></style>