<template>
    <div>
        <div class="my-20">
            <h4 class="text-dgl-primary font-bold text-center font-dm py-3 ">NOS PRODUITS</h4>
            <h2 class="font-dm font-bold text-[30px] md:mx-[360px] text-center pb-8">Des fonctionnalités puissantes pour
                décupler
                votre
                productivité
            </h2>
            <div class="flex items-center justify-center">
                <button
                    :class="{ 'bg-dgl-primary': activeTab === 'category1', 'text-white': activeTab === 'category1', 'bg-white, border-[1px] border-blue-300': activeTab !== 'category1' }"
                    @click="setActiveTab('category1')"
                    class="px-[100px] text-[20px] mr-3 font-dm font-bold py-[15px] m-2 rounded-[13px] cursor-pointer ease-in-out duration-700 transition-all ">
                    Applications DGL
                </button>
                <button
                    :class="{ 'bg-dgl-primary': activeTab === 'category2', 'text-white': activeTab === 'category2', 'bg-white, border-[1px] border-blue-300': activeTab !== 'category2' }"
                    @click="setActiveTab('category2')"
                    class="px-[100px] text-[20px] ml-3 font-bold py-[15px] m-2 rounded-[13px] cursor-pointer ease-in-out duration-700 transition-all ">
                    Vente des Matériels
                </button>
            </div>

            <div v-if="activeTab === 'category1'" class="ease-in-out duration-1000 transition-all ">

                <div
                    class="grid grid-cols-2 bg-blue-100 h-[450px] gap-12 w-full mt-16 p-[50px] ease-in-out duration-700 transition-all  ">
                    <div>
                        <h4
                            class="text-dgl-primary text-[24px] font-bold text-left font-dm py-6 pl-8 ease-in-out duration-700 transition-all ">
                            Applications DGL
                            pour les Chauffeurs</h4>
                        <h2 class="font-sans text-[20px] text-left pb-6 pl-8 ease-in-out duration-700 transition-all ">
                            Nos applications DGL sont conçues spécialement pour les chauffeurs.
                            Elles simplifient la gestion des trajets, fournissent des informations
                            en temps réel et améliorent l'efficacité des opérations de livraison.
                            Que vous soyez un chauffeur indépendant ou que vous travailliez au sein
                            d'une flotte,nos applications vous aideront à optimiser votre travail sur la route.
                        </h2>
                        <AppBoutons class="pl-8">
                            Contactez-nous
                        </AppBoutons>
                    </div>

                    <div class="">
                        <img src="./../public/AppDglChauffeur.svg" class="pl-16 w-[558px] h-[350px] rounded-[14px]" alt="">
                    </div>
                </div>

                <div class="grid grid-cols-2 h-[450px] gap-12 w-full mt-10 p-[50px] ">
                    <div class="rounded-[14px]">
                        <img src="./../public/CommandeCourses.svg" class="pl-10 w-[558px] h-[350px] rounded-[14px]" alt="">
                    </div>

                    <div>
                        <h4
                            class="text-dgl-primary text-[24px] font-bold text-left font-dm py-6 pl-8 ease-in-out duration-700 transition-all ">
                            Les commandes pour
                            les courses
                        </h4>
                        <h2 class="font-sans text-[20px] text-left pb-6 pl-8 ease-in-out duration-700 transition-all ">
                            Nos commandeurs sont l'outil parfait pour organiser et gérer les courses de
                            livraison. Avec des fonctionnalités avancées de planification de trajet
                            et de suivi des colis, vous pouvez garantir des livraisons rapides
                            et précises à chaque fois. Simplifiez votre processus
                            de commande et offrez une expérience client exceptionnelle.
                        </h2>
                        <AppBoutons class="pl-8">
                            Contactez-nous
                        </AppBoutons>
                    </div>
                </div>
                <div
                    class="grid grid-cols-2 bg-blue-100 h-[450px] gap-12 w-full mt-10 p-[50px] ease-in-out duration-700 transition-all  ">
                    <div>
                        <h4
                            class="text-dgl-primary text-[24px] font-bold text-left font-dm py-6 pl-8 ease-in-out duration-700 transition-all ">
                            Applications de
                            gestion de Flotte
                        </h4>
                        <h2 class="font-sans text-[20px] text-left pb-6 pl-8 ease-in-out duration-700 transition-all ">
                            Avec une interface conviviale et des fonctionnalités avancées,
                            vous pouvez suivre en temps réel l'emplacement de vos véhicules,
                            gérer les itinéraires, et même améliorer la communication avec
                            vos conducteurs. Simplifiez votre gestion de flotte dès
                            aujourd'hui avec les applications DGL.
                        </h2>
                        <AppBoutons class="pl-8 ease-in-out duration-700 transition-all ">
                            Contactez-nous
                        </AppBoutons>
                    </div>

                    <div class="">
                        <img src="./../public/AppGestionFlotte.svg" class="pl-16 w-[558px] h-[350px] rounded-[14px]" alt="">
                    </div>
                </div>
            </div>
            <div v-if="activeTab === 'category2'" class="ease-in-out duration-1000 transition-all ">

                <div
                    class="grid grid-cols-2 bg-blue-100 h-[450px] gap-12 w-full mt-16 p-[50px] ease-in-out duration-700 transition-all  ">
                    <div>
                        <h4 class="text-dgl-primary text-[24px] font-bold text-left font-dm py-6 pl-8 ">Module GPS</h4>
                        <h2 class="font-sans text-[20px] text-left pb-6 pl-8">
                            Nos modules GPS utilisent les signaux satellites les plus avancés
                            pour vous offrir une précision de localisation incomparable, que ce soit
                            pour la navigation automobile, la géolocalisation de flottes,
                            le suivi d'actifs ou tout autre besoin. Ils sont conçus pour être
                            faciles à intégrer dans une large gamme d'applications.
                        </h2>
                        <AppBoutons class="pl-8">
                            Contactez-nous
                        </AppBoutons>
                    </div>

                    <div class="">
                        <img src="./../public/ModuleGPS.svg" class="pl-16 w-[558px] h-[350px] rounded-[14px]" alt="">
                    </div>
                </div>

                <div class="grid grid-cols-2 h-[450px] gap-12 w-full mt-10 p-[50px]  ">
                    <div class="">
                        <img src="./../public/DispoPesage.svg" class="pl-16 w-[558px] h-[350px] rounded-[14px]" alt="">

                    </div>

                    <div>
                        <h4 class="text-dgl-primary text-[24px] font-bold text-left font-dm py-6 pl-8 ">Dispositif de pesage
                        </h4>
                        <h2 class="font-sans text-[20px] text-left pb-6 pl-8">
                            Avec des fonctionnalités avancées et une technologie de pointe,
                            nos dispositifs de pesage vous permettent d'optimiser vos opérations
                            et de garantir la qualité de vos produits..Nos dispositifs sont
                            conviviaux et simples à intégrer dans votre environnement de travail.
                            Nous proposons une gamme de modèles pour répondre à diverses exigences.
                        </h2>
                        <AppBoutons class="pl-8">
                            Contactez-nous
                        </AppBoutons>
                    </div>
                </div>
                <div class="grid grid-cols-2 bg-blue-100 h-[450px] gap-12 w-full mt-10 p-[50px]  ">
                    <div>
                        <h4 class="text-dgl-primary text-[24px] font-bold text-left font-dm py-6 pl-8 ">Coffres intelligents
                        </h4>
                        <h2 class="font-sans text-[20px] text-left pb-6 pl-8">
                            Nos coffres intelligents utilisent la technologie de pointe pour
                            assurer la sécurité maximale de vos biens. Grâce à des systèmes
                            de verrouillage avancés et à une surveillance en temps réel, vous
                            pouvez avoir l'esprit tranquille.
                        </h2>
                        <AppBoutons class="pl-8">
                            Contactez-nous
                        </AppBoutons>
                    </div>

                    <div class="">
                        <img src="./../public/CoffresIntellignent.svg" class="pl-16 w-[558px] h-[350px] rounded-[14px]"
                            alt="">
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
import { ref, computed } from 'vue';

const activeTab = ref('category1');


const setActiveTab = (category) => {
    activeTab.value = category;
};
</script>



















