<template>
    <div class="w-full max-w-[600px] mx-auto mb-16">

        <h1 class="text-center text-dgl-primary font-bold text-[26px] font-dm pb-16">Comment procédons-nous?</h1>

        <!-- Ligne 1 -->
        <div>
            <div @click="toggleAccordion(1)"
                class="cursor-pointer p-4 border-t-3 border-b-3 border-blue-200  transition duration-300">
                <div class="flex items-center justify-between">
                    <div class="flex items-center">
                        <h3 class="text-[20px]" :class="{ 'font-bold text-[20px] text-dgl-primary': isAccordionOpen[1] }">
                            Flux de
                            communication</h3>
                    </div>
                    <div>
                        <img v-if="isAccordionOpen[1]" src="./../public/moin.svg" class="w-4 h-4 fill-current text-lg"
                            :class="{ 'text-dgl-primary': isAccordionOpen[1] }" alt="">
                        <img v-else src="./../public/plus.svg" class="w-4 h-4 fill-current text-lg">
                    </div>
                </div>
            </div>
            <div v-if="isAccordionOpen[1]" class="p-4 bg-white">
                <p class="text-black font-sans text-[20px] duration-1000 transition-all ease-in-out">
                    Vitae congue eu consequat ac felis placerat vestibulum
                    lectus mauris ultrices. Cursus sit amet dictum sit amet
                    justo donec enim
                    diam porttitor lacus luctus accumsan tortor posuere.</p>
            </div>
        </div>

        <!-- Ligne 2 -->


        <div @click="toggleAccordion(2)"
            class="cursor-pointer p-4 border-t-2 border-b-3 border-blue-200 transition duration-300">
            <div class="flex items-center justify-between">
                <div class="flex items-center">
                    <h3 class="text-[20px]" :class="{ 'font-bold text-[20px]  text-dgl-primary': isAccordionOpen[2] }">
                        Aquisition de
                        véhicules</h3>
                </div>
                <div>
                    <img v-if="isAccordionOpen[2]" src="./../public/moin.svg" class="w-4 h-4 fill-current text-lg"
                        :class="{ 'text-dgl-primary': isAccordionOpen[2] }" alt="">
                    <img v-else src="./../public/plus.svg" class="w-4 h-4 fill-current text-lg">
                </div>
            </div>
        </div>
        <div v-if="isAccordionOpen[2]" class="p-4 bg-white">
            <p class="text-black font-sans text-[20px] duration-1000 transition-all ease-in-out">
                Vitae congue eu consequat ac felis placerat vestibulum
                lectus mauris ultrices. Cursus sit amet dictum sit amet
                justo donec enim
                diam porttitor lacus luctus accumsan tortor posuere.</p>
        </div>
        <!-- Ligne 3 -->
        <div @click="toggleAccordion(3)"
            class="cursor-pointer p-4 border-t-2 border-b-3 border-blue-200  transition duration-300">
            <div class="flex items-center justify-between">
                <div class="flex items-center">
                    <h3 class="text-[22px]" :class="{ 'font-bold text-[20px] text-dgl-primary': isAccordionOpen[3] }">
                        Gestion des
                        réparations et de maintenance corrective</h3>
                </div>
                <div>
                    <img v-if="isAccordionOpen[3]" src="./../public/moin.svg" class="w-4 h-4 fill-current text-lg"
                        :class="{ 'text-dgl-primary': isAccordionOpen[3] }" alt="">
                    <img v-else src="./../public/plus.svg" class="w-4 h-4 fill-current text-lg">
                </div>
            </div>
        </div>
        <div v-if="isAccordionOpen[3]" class="p-4 bg-white">
            <p class="text-black font-sans text-[20px] duration-1000 transition-all ease-in-out">
                Vitae congue eu consequat ac felis placerat vestibulum
                lectus mauris ultrices. Cursus sit amet dictum sit amet
                justo donec enim
                diam porttitor lacus luctus accumsan tortor posuere.</p>
        </div>

        <!-- Ligne 4 -->
        <div @click="toggleAccordion(4)"
            class="cursor-pointer p-4 border-t-2 border-b-3 border-blue-200  transition duration-300">
            <div class="flex items-center justify-between">
                <div class="flex items-center">
                    <h3 class="text-[20px]" :class="{ 'font-bold text-[20px] text-dgl-primary': isAccordionOpen[4] }">
                        Gestion des
                        documents et de la conformité </h3>
                </div>
                <div>
                    <img v-if="isAccordionOpen[4]" src="./../public/moin.svg" class="w-4 h-4 fill-current text-lg"
                        :class="{ 'text-dgl-primary': isAccordionOpen[4] }" alt="">
                    <img v-else src="./../public/plus.svg" class="w-4 h-4 fill-current text-lg">
                </div>
            </div>
        </div>
        <div v-if="isAccordionOpen[4]" class="p-4 bg-white">
            <p class="text-black font-sans text-[20px] duration-1000 transition-all ease-in-out">
                Vitae congue eu consequat ac felis placerat vestibulum
                lectus mauris ultrices. Cursus sit amet dictum sit amet
                justo donec enim
                diam porttitor lacus luctus accumsan tortor posuere.</p>
        </div>

        <!-- Ligne 5 -->
        <div @click="toggleAccordion(5)"
            class="cursor-pointer p-4 border-t-2 border-b-3 border-blue-200  transition duration-300">
            <div class="flex items-center justify-between">
                <div class="flex items-center">
                    <h3 class="text-[20px]" :class="{ 'font-bold text-[20px] text-dgl-primary': isAccordionOpen[5] }">
                        Sécurité</h3>
                </div>
                <div>
                    <img v-if="isAccordionOpen[5]" src="./../public/moin.svg" class="w-4 h-4 fill-current text-lg"
                        :class="{ 'text-dgl-primary': isAccordionOpen[5] }" alt="">
                    <img v-else src="./../public/plus.svg" class="w-4 h-4 fill-current text-lg">
                </div>
            </div>
        </div>
        <div v-if="isAccordionOpen[5]" class="p-4 bg-white">
            <p class="text-black font-sans text-[20px] duration-1000 transition-all ease-in-out">
                Vitae congue eu consequat ac felis placerat vestibulum
                lectus mauris ultrices. Cursus sit amet dictum sit amet
                justo donec enim
                diam porttitor lacus luctus accumsan tortor posuere.</p>
        </div>

    </div>
</template>

<script>
export default {
    data() {
        return {
            isAccordionOpen: {
                1: true,
                2: false,
                3: false,
                4: false,
                5: false
                // Ajoutez les autres lignes ici
            },
        };
    },
    methods: {
        toggleAccordion(line) {
            // Fermez toutes les lignes sauf celle actuellement cliquée
            for (let key in this.isAccordionOpen) {
                if (key != line) {
                    this.isAccordionOpen[key] = false;
                }
            }
            this.isAccordionOpen[line] = !this.isAccordionOpen[line];
        },
    },
};
</script>
