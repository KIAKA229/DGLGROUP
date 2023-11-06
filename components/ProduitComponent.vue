<template>
    <div>
        <div class="my-6 md:my-20 ">
            <h4 class="text-dgl-primary font-bold text-center font-dm py-3 ">NOS PRODUITS</h4>
            <h2 class="font-dm font-bold text-[30px] md:mx-[360px] text-center d:pb-8 hidden sm:block">Des fonctionnalités
                puissantes pour
                décupler
                votre
                productivité
            </h2>
            <div class="flex items-center justify-center px-6">
                <div>
                    <button
                        :class="{ 'bg-dgl-primary': activeTab === 'category1', 'text-white': activeTab === 'category1', 'bg-white, border-[1px] border-blue-300': activeTab !== 'category1' }"
                        @click="setActiveTab('category1')"
                        class="md:px-[100px] px-4 py-3 text-md md:text-[20px] mr-3 font-dm font-bold md:py-[15px] m-2 rounded-[13px] cursor-pointer ease-in-out duration-700 transition-all "
                        style="white-space: nowrap;">
                        Applications DGL
                    </button>
                </div>
                <div>
                    <button
                        :class="{ 'bg-dgl-primary': activeTab === 'category2', 'text-white': activeTab === 'category2', 'bg-white, border-[1px] border-blue-300': activeTab !== 'category2' }"
                        @click="setActiveTab('category2')"
                        class="md:px-[100px] px-4 py-3 text-md md:text-[20px] mr-3 font-dm font-bold md:py-[15px] m-2 rounded-[13px] cursor-pointer ease-in-out duration-700 transition-all capitalize"
                        style="white-space: nowrap;">
                        Vente des Matériels
                    </button>
                </div>


            </div>

            <div v-if="activeTab === 'category1'" class="ease-in-out duration-1000 transition-all ">

                <div
                    class="grid grid-cols-1 md:grid-cols-2 h-auto  bg-blue-100 md:h-[450px] gap-12 w-full mt-16 px-6  md:py-[30px] ease-in-out duration-700 transition-all  ">
                    <div>
                        <h4 class="text-dgl-primary text-[24px] font-bold text-left font-dm py-[30px] pl-1 md:pl-8 ">
                            Applications DGL
                            pour les Chauffeurs
                        </h4>
                        <div class="">
                            <img src="./../public/AppDglChauffeur.svg" class="block sm:hidden w-[558px] py-8 rounded-[14px]"
                                alt="">
                        </div>
                        <h2 class="font-sans text-[20px] text-left pb-2 md:pb-4 pl-1 md:pl-8 ">
                            Nos applications DGL sont conçues spécialement pour les chauffeurs.
                            Elles simplifient la gestion des trajets, fournissent des informations
                            en temps réel et améliorent l'efficacité des opérations de livraison.
                            Que vous soyez un chauffeur indépendant ou que vous travailliez au sein
                            d'une flotte,nos applications vous aideront à optimiser votre travail sur la route.
                        </h2>
                        <AppBoutons class="pt-4 pl-1 md:pl-8">
                            Contactez-nous
                        </AppBoutons>
                    </div>

                    <div class="pl-1 md:pl-8">
                        <img src="./../public/AppDglChauffeur.svg"
                            class="pl-16 w-[558px] h-[350px] rounded-[14px] hidden sm:block" alt="">
                    </div>
                </div>

                <div
                    class="grid grid-cols-1 md:grid-cols-2 h-auto md:h-[450px] md:gap-12 w-full mt-16 px-6 md:p-[30px] md:pb-10 ease-in-out duration-700 transition-all  ">

                    <div class="">
                        <img src="./../public/CommandeCourses.svg" class="w-[558px] py-8 rounded-[14px]  hidden sm:block"
                            alt="">
                    </div>

                    <div>
                        <h4 class="text-dgl-primary text-[24px] font-bold text-left font-dm py-[30px] pl-1 md:pl-8 ">
                            Les commandes pour
                            les courses
                        </h4>
                        <div class="">
                            <img src="./../public/CommandeCourses.svg" class="w-[558px] py-8 rounded-[14px] block sm:hidden"
                                alt="">
                        </div>
                        <h2 class="font-sans text-[20px] text-left pb-6 pl-1 md:pl-8">
                            Nos applications DGL sont conçues spécialement pour les chauffeurs.
                            Elles simplifient la gestion des trajets, fournissent des informations
                            en temps réel et améliorent l'efficacité des opérations de livraison.
                            Que vous soyez un chauffeur indépendant ou que vous travailliez au sein
                            d'une flotte,nos applications vous aideront à optimiser votre travail sur la route.
                        </h2>
                        <AppBoutons class=" pl-1 md:pl-8">
                            Contactez-nous
                        </AppBoutons>
                    </div>
                </div>
                <div
                    class="grid grid-cols-1 md:grid-cols-2 h-auto  bg-blue-100 md:h-[450px] py-10 gap-12 w-full mt-16 px-6 md:p-[30px] ease-in-out duration-700 transition-all  ">

                    <div>
                        <h4
                            class="text-dgl-primary text-[24px] font-bold text-left font-dm pb-1 md:pb-1 md:pt-8 pt-1 pl-1 md:pl-8 ">
                            Applications de
                            gestion de Flotte
                        </h4>
                        <div class="">
                            <img src="./../public/AppGestionFlotte.svg"
                                class="w-[558px] py-8 rounded-[14px] block sm:hidden" alt="">
                        </div>
                        <h2 class="font-sans text-[20px] text-left pb-6 md:pt-4 pt-0 pl-1 md:pl-8">
                            Avec une interface conviviale et des fonctionnalités avancées,
                            vous pouvez suivre en temps réel l'emplacement de vos véhicules,
                            gérer les itinéraires, et même améliorer la communication avec
                            vos conducteurs. Simplifiez votre gestion de flotte dès
                            aujourd'hui avec les applications DGL.
                        </h2>

                        <AppBoutons class="md:pt-2 pt-1 pl-1 md:pl-8">
                            Contactez-nous
                        </AppBoutons>
                    </div>

                    <div class="">
                        <img src="./../public/AppGestionFlotte.svg"
                            class="hidden sm:block pl-16 w-[558px] h-[350px] rounded-[14px] md:pt-6" alt="">
                    </div>
                </div>
            </div>
            <div v-if="activeTab === 'category2'" class="ease-in-out duration-1000 transition-all ">

                <div
                    class="grid grid-cols-1 md:grid-cols-2 h-auto  bg-blue-100 md:h-[450px] gap-12 w-full mt-16 px-6  md:py-[30px] ease-in-out duration-700 transition-all  ">
                    <div>
                        <h4 class="text-dgl-primary text-[24px] font-bold text-left font-dm py-[30px] pl-1 md:pl-8 ">
                            Module GPS
                        </h4>
                        <div class="">
                            <img src="./../public/ModuleGPS.svg" class="block sm:hidden w-[558px] py-8 rounded-[14px]"
                                alt="">
                        </div>
                        <h2 class="font-sans text-[20px] text-left pb-2 md:pb-4 pl-1 md:pl-8 ">
                            Nos modules GPS utilisent les signaux satellites les plus avancés
                            pour vous offrir une précision de localisation incomparable, que ce soit
                            pour la navigation automobile, la géolocalisation de flottes,
                            le suivi d'actifs ou tout autre besoin. Ils sont conçus pour être
                            faciles à intégrer dans une large gamme d'applications.
                        </h2>
                        <AppBoutons class="pt-4 pl-1 md:pl-8">
                            Contactez-nous
                        </AppBoutons>
                    </div>

                    <div class="pl-1 md:pl-8">
                        <img src="./../public/ModuleGPS.svg"
                            class="pl-16 w-[558px] h-[350px] rounded-[14px] hidden sm:block" alt="">
                    </div>
                </div>

                <div
                    class="grid grid-cols-1 md:grid-cols-2 h-auto md:h-[450px] md:gap-12 w-full mt-16 px-6 md:p-[30px] md:pb-10 ease-in-out duration-700 transition-all  ">

                    <div class="">
                        <img src="./../public/DispoPesage.svg" class="w-[558px] py-8 rounded-[14px]  hidden sm:block"
                            alt="">
                    </div>

                    <div>
                        <h4 class="text-dgl-primary text-[24px] font-bold text-left font-dm py-[30px] pl-1 md:pl-8 ">
                            Dispositif de pesage
                        </h4>
                        <div class="">
                            <img src="./../public/DispoPesage.svg" class="w-[558px] py-8 rounded-[14px] block sm:hidden"
                                alt="">
                        </div>
                        <h2 class="font-sans text-[20px] text-left pb-6 pl-1 md:pl-8">
                            Avec des fonctionnalités avancées et une technologie de pointe,
                            nos dispositifs de pesage vous permettent d'optimiser vos opérations
                            et de garantir la qualité de vos produits..Nos dispositifs sont
                            conviviaux et simples à intégrer dans votre environnement de travail.
                            Nous proposons une gamme de modèles pour répondre à diverses exigences.
                        </h2>
                        <AppBoutons class=" pl-1 md:pl-8">
                            Contactez-nous
                        </AppBoutons>
                    </div>
                </div>
                <div
                    class="grid grid-cols-1 md:grid-cols-2 h-auto  bg-blue-100 md:h-[450px] py-10 gap-12 w-full mt-16 px-6 md:p-[30px] ease-in-out duration-700 transition-all  ">

                    <div>
                        <h4
                            class="text-dgl-primary text-[24px] font-bold text-left font-dm pb-1 md:pb-1 md:pt-8 pt-1 pl-1 md:pl-8 ">
                            Coffres
                            intelligents
                        </h4>
                        <div class="">
                            <img src="./../public/CoffresIntellignent.svg"
                                class="w-[558px] py-8 rounded-[14px] block sm:hidden" alt="">
                        </div>
                        <h2 class="font-sans text-[20px] text-left pb-6 md:pt-4 pt-0 pl-1 md:pl-8">
                            Nos coffres intelligents utilisent la technologie de pointe pour
                            assurer la sécurité maximale de vos biens. Grâce à des systèmes
                            de verrouillage avancés et à une surveillance en temps réel, vous
                            pouvez avoir l'esprit tranquille.Grâce à des systèmes
                            de verrouillage avancés et à une surveillance en temps réel, vous
                            pouvez avoir l'esprit tranquille.
                        </h2>

                        <AppBoutons class="md:pt-2 pt-1 pl-1 md:pl-8">
                            Contactez-nous
                        </AppBoutons>
                    </div>

                    <div class="">
                        <img src="./../public/CoffresIntellignent.svg"
                            class="hidden sm:block pl-16 w-[558px] h-[350px] rounded-[14px] md:pt-6" alt="">
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



















