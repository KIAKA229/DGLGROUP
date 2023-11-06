<template>
    <div>
        <div class="my-16 ">
            <h4 class="text-dgl-primary font-bold text-center font-dm py-8 text-[26px]  ">Nos Services de Mobilité</h4>

            <div class="flex items-center justify-center mx-6">
                <button
                    :class="{ 'bg-dgl-primary': activeTab === 'category1', 'text-white': activeTab === 'category1', 'bg-white, border-[1px] border-blue-300': activeTab !== 'category1' }"
                    @click="setActiveTab('category1')"
                    class="px-[50px] mr-1 font-sans text-[20px] py-[15px] m-2 rounded-[13px] cursor-pointer ease-in-out duration-700 transition-all">
                    Logistique
                </button>
                <button
                    :class="{ 'bg-dgl-primary': activeTab === 'category2', 'text-white': activeTab === 'category2', 'bg-white, border-[1px] border-blue-300': activeTab !== 'category2' }"
                    @click="setActiveTab('category2')"
                    class="px-[30px] mr-1 font-sans text-[20px] py-[15px] m-2 rounded-[13px] cursor-pointer ease-in-out duration-700 transition-all">
                    Vente de vehicule
                </button>
                <button
                    :class="{ 'bg-dgl-primary': activeTab === 'category3', 'text-white': activeTab === 'category3', 'bg-white, border-[1px] border-blue-300': activeTab !== 'category3' }"
                    @click="setActiveTab('category3')"
                    class="px-[30px] mr-1  font-sans text-[20px] py-[15px] m-2 rounded-[13px] cursor-pointer ease-in-out duration-700 transition-all">
                    Gestion de flottes
                </button>
                <button
                    :class="{ 'bg-dgl-primary': activeTab === 'category4', 'text-white': activeTab === 'category4', 'bg-white, border-[1px] border-blue-300': activeTab !== 'category4' }"
                    @click="setActiveTab('category4')"
                    class="px-[70px] mr-1 font-sans text-[20px] py-[15px] m-2 rounded-[13px] cursor-pointer ease-in-out duration-700 transition-all">
                    VTC
                </button>
                <button
                    :class="{ 'bg-dgl-primary': activeTab === 'category5', 'text-white': activeTab === 'category5', 'bg-white, border-[1px] border-blue-300': activeTab !== 'category5' }"
                    @click="setActiveTab('category5')"
                    class="px-[30px] mr-1 font-sans text-[20px] py-[15px] m-2 rounded-[13px] cursor-pointer ease-in-out duration-700 transition-all">
                    Traçage et Suivie
                </button>
                <button
                    :class="{ 'bg-dgl-primary': activeTab === 'category6', 'text-white': activeTab === 'category6', 'bg-white, border-[1px] border-blue-300': activeTab !== 'category2' }"
                    @click="setActiveTab('category6')"
                    class="px-[50px] mr-1 font-sans text-[20px] py-[15px] m-2 rounded-[13px] cursor-pointer ease-in-out duration-700 transition-all">
                    Livraison
                </button>
            </div>

            <div v-if="activeTab === 'category1'" class="ease-in-out duration-1000 transition-all ">
                <div
                    class="grid grid-cols-2 pt-20 bg-blue-100 h-[500px] gap-5 w-full mt-16 px-[40px] ease-in-out duration-700 transition-all ">
                    <div>
                        <h4
                            class="text-dgl-primary text-[22px] font-bold text-left font-dm py-4 pl-8 ease-in-out duration-700 transition-all">
                            Transport et
                            Logistique</h4>
                        <h2 class="font-sans text-left pb-8 pl-8 text-[20px] pt-2 ease-in-out duration-700 transition-all">
                            Chez DGL, nous sommes fiers de proposer des solutions de
                            transport et de logistique de classe mondiale.Notre expertise
                            en matière de logistique et notre flotte de véhicules modernes
                            nous permettent de répondre à vos besoins en matière de
                            transport de manière efficace et fiable.
                        </h2>
                        <AppBoutons class="pl-8 ">
                            Contactez-nous
                        </AppBoutons>
                    </div>

                    <div class="px-10">

                        <CarrouselProduit />

                    </div>
                </div>
            </div>
            <div v-else-if="activeTab === 'category2'" class="ease-in-out duration-1000 transition-all ">
                <div
                    class="grid grid-cols-2 pt-20 bg-blue-100 h-[500px] gap-5 w-full mt-16 px-[40px] ease-in-out duration-700 transition-all ">
                    <div>
                        <h4
                            class="text-dgl-primary text-[22px] font-bold text-left font-dm py-4 pl-8 ease-in-out duration-700 transition-all">
                            Vente de vehicule
                        </h4>
                        <h2 class="font-sans text-left pb-8 pl-8 text-[20px] pt-2 ease-in-out duration-700 transition-all">
                            Que vous recherchiez une voiture familiale spacieuse, un véhicule tout-terrain robuste ou
                            une
                            voiture économe en carburant, notre équipe dévouée est là pour vous guider dans votre choix.
                            Chez AutoChoice, la qualité et le service sont notre priorité numéro un. Faites le premier
                            pas
                            vers la voiture de vos rêves en nous rendant visite aujourd'hui.
                        </h2>
                        <AppBoutons class="pl-8">
                            Contactez-nous
                        </AppBoutons>
                    </div>

                    <div class="px-10">
                        <div class="px-10">
                            <img src="./../public/AppDglChauffeur.svg" class=" w-[550px] h-[350px] rounded-[14px]" alt="">

                        </div>
                    </div>
                </div>
            </div>
            <div v-else-if="activeTab === 'category3'" class="ease-in-out duration-1000 transition-all ">
                <div
                    class="grid grid-cols-2 pt-20 bg-blue-100 h-[500px] gap-5 w-full mt-16 px-[40px] ease-in-out duration-700 transition-all ">
                    <div>
                        <h4
                            class="text-dgl-primary text-[22px] font-bold text-left font-dm py-4 pl-8 ease-in-out duration-700 transition-all">
                            Gestion de Flottes
                        </h4>
                        <h2 class="font-sans text-left pb-8 pl-8 text-[20px] pt-2 ease-in-out duration-700 transition-all">
                            Grâce à notre expertise et à notre technologie de pointe, vous pourrez prendre des décisions
                            éclairées pour votre flotte, tout en offrant à vos conducteurs une expérience plus sûre et
                            plus
                            efficace sur la route. Faites confiance à XYZ Fleet Management pour gérer votre flotte, afin
                            que
                            vous puissiez vous concentrer sur ce qui compte le plus pour votre entreprise.
                        </h2>
                        <AppBoutons class="pl-8 ">
                            Contactez-nous
                        </AppBoutons>
                    </div>

                    <div class="px-10">
                        <div class="px-10">
                            <img src="./../public/CoffresIntellignent.svg" class=" w-[550px] h-[350px] rounded-[14px]"
                                alt="">

                        </div>
                    </div>
                </div>
            </div>
            <div v-else-if="activeTab === 'category4'" class="ease-in-out duration-1000 transition-all ">
                <div
                    class="grid grid-cols-2 pt-20 bg-blue-100 h-[500px] gap-5 w-full mt-16 px-[40px] ease-in-out duration-700 transition-all ">
                    <div>
                        <h4
                            class="text-dgl-primary text-[22px] font-bold text-left font-dm py-4 pl-8 ease-in-out duration-700 transition-all">
                            VTC
                        </h4>
                        <h2 class="font-sans text-left pb-8 pl-8 text-[20px] pt-2 ease-in-out duration-700 transition-all">
                            Chez DGL, nous sommes déterminés à vous offrir une expérience de transport exceptionnelle à
                            chaque trajet. Nos chauffeurs professionnels et courtois sont prêts à vous conduire en toute
                            sécurité et confort, que ce soit pour un rendez-vous d'affaires, une soirée en ville ou un
                            trajet vers l'aéroport. Faites de chaque trajet une expérience mémorable avec EliteRide.
                        </h2>
                        <AppBoutons class="pl-8 ">
                            Contactez-nous
                        </AppBoutons>
                    </div>

                    <div class="px-10">
                        <div class="px-10">

                            <img src="./../public/BestProduit1.svg" class=" w-[550px] h-[350px] rounded-[14px]" alt="">

                        </div>
                    </div>
                </div>
            </div>
            <div v-else-if="activeTab === 'category5'" class="ease-in-out duration-1000 transition-all ">
                <div
                    class="grid grid-cols-2 pt-20 bg-blue-100 h-[500px] gap-5 w-full mt-16 px-[40px] ease-in-out duration-700 transition-all ">
                    <div>
                        <h4
                            class="text-dgl-primary text-[22px] font-bold text-left font-dm py-4 pl-8 ease-in-out duration-700 transition-all">
                            Traçage et Suivie
                        </h4>
                        <h2 class="font-sans text-left pb-8 pl-8 text-[20px] pt-2">
                            Lorsqu'il s'agit de traçage précis et fiable, faites confiance à l'expertise de notre
                            entreprise. Chez DGL, nous avons perfectionné l'art du traçage pour répondre à vos besoins
                            les
                            plus exigeants. Notre technologie de pointe et notre équipe de professionnels dévoués sont
                            là
                            pour vous.
                        </h2>
                        <AppBoutons class="pl-8 ">
                            Contactez-nous
                        </AppBoutons>
                    </div>

                    <div class="px-10">
                        <div class="px-10">

                            <img src="./../public/BestProduit2 (1).svg" class=" w-[550px] h-[350px] rounded-[14px]" alt="">

                        </div>
                    </div>
                </div>
            </div>
            <div v-else class="ease-in-out duration-1000 transition-all ">
                <div
                    class="grid grid-cols-2 pt-20 bg-blue-100 h-[500px] gap-5 w-full mt-16 px-[40px] ease-in-out duration-700 transition-all ">
                    <div>
                        <h4
                            class="text-dgl-primary text-[22px] font-bold text-left font-dm py-4 pl-8 ease-in-out duration-700 transition-all">
                            Livraison</h4>
                        <h2 class="font-sans text-left pb-8 pl-8 text-[20px] pt-2">
                            Notre équipe expérimentée et notre réseau de livraison efficace garantissent que vos colis
                            arrivent à destination en toute sécurité et dans les délais convenus. Que ce soit pour des
                            livraisons locales ou internationales, nous nous engageons à répondre à vos besoins de
                            manière
                            rapide, fiable et professionnelle.
                        </h2>
                        <AppBoutons class="pl-8 ">
                            Contactez-nous
                        </AppBoutons>
                    </div>

                    <div class="px-10">
                        <div class="px-10">

                            <img src="./../public/BestProduit2.svg" class=" w-[550px] h-[350px] rounded-[14px]" alt="">

                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
import { ref, computed } from 'vue';
import { onMounted } from 'vue'
import { initFlowbite } from 'flowbite'

const activeTab = ref('category1');

onMounted(() => {
    initFlowbite();
})

const setActiveTab = (category) => {
    activeTab.value = category;
};


</script>



















