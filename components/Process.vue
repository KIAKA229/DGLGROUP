<template>
    <div class=" my-20 text-center ">

        <div class="flex justify-center items-center space-x-16 z-30">
            <img class="cursor-pointer" @click="scrollYear(-1)" :disabled="isFirstYear"
                src="./../public/processPrevious.svg" alt="">

            <div class="relative hidden sm:block">
                <div class="flex items-center space-x-16">
                    <button v-for="year in visibleYears" :key="year" @click="selectYearAndScroll(year)" :class="[
                        'btn',
                        'mx-8', // Espacement horizontal entre les boutons
                        {
                            'active-btn': year === selectedYear,
                        },
                    ]">
                        {{ year }}
                    </button>
                </div>
                <div class="line"></div>
            </div>

            <div class="relative block sm:hidden">
                <div class="flex items-center space-x-16">
                    <button v-for="year in visibleYears" :key="year" @click="selectYear(year)" :class="[
                        'btn mx-8',
                        {
                            'active-btn': year === selectedYear,
                        },
                    ]">
                        {{ year }}
                    </button>
                </div>
                <div class="line"></div>
            </div>



            <img class="cursor-pointer" @click="scrollYear(1)" :disabled="isLastYear" src="./../public/processNext.svg"
                alt="">
        </div>

        <div>
            <div class="description mt-8 " v-if="years[0]">
                <p class="md:mx-[200px] mx-auto text-[20px] text-center">
                    Notre mission est de simplifier la gestion de flotte et
                    de rendre le processus d'importation de véhicules
                    plus efficace pour nos clients. Nous croyons fermement
                    que la technologie peut améliorer chaque aspect de
                    ces opérations
                </p>
            </div>
            <div class="description mt-10 " v-else-if="years[1]">
                <p class="md:mx-[200px] mx-auto text-[20px] text-center">
                    Notre mission est de simplifier la gestion de flotte et
                    de rendre le processus d'importation de véhicules
                    plus efficace pour nos clients. Nous croyons fermement
                    que la technologie peut améliorer chaque aspect de
                    ces opérations
                </p>
            </div>
            <div class="description mt-10 " v-else-if="years[2]">
                <p class="md:mx-[200px] mx-auto text-[20px] text-center">
                    Notre mission est de simplifier la gestion de flotte et
                    de rendre le processus d'importation de véhicules
                    plus efficace pour nos clients. Nous croyons fermement
                    que la technologie peut améliorer chaque aspect de
                    ces opérations
                </p>
            </div>
            <div class="description mt-10 " v-else-if="years[3]">
                <p>
                    Notre mission est de simplifier la gestion de flotte et
                    de rendre le processus d'importation de véhicules
                    plus efficace pour nos clients. Nous croyons fermement
                    que la technologie peut améliorer chaque aspect de
                    ces opérations
                </p>
            </div>
            <div class="description mt-10 " v-else-if="years[4]">
                <p class="md:mx-[200px] mx-auto text-[20px] text-center">
                    Notre mission est de simplifier la gestion de flotte et
                    de rendre le processus d'importation de véhicules
                    plus efficace pour nos clients. Nous croyons fermement
                    que la technologie peut améliorer chaque aspect de
                    ces opérations
                </p>
            </div>
            <div class="description mt-10 " v-else-if="years[5]">
                <p class="md:mx-[200px] mx-auto text-[20px] text-center">
                    Notre mission est de simplifier la gestion de flotte et
                    de rendre le processus d'importation de véhicules
                    plus efficace pour nos clients. Nous croyons fermement
                    que la technologie peut améliorer chaque aspect de
                    ces opérations
                </p>
            </div>
            <div class="description mt-10 " v-else>
                <p class="md:mx-[200px] mx-auto text-[20px] text-center">
                    Notre mission est de simplifier la gestion de flotte et
                    de rendre le processus d'importation de véhicules
                    plus efficace pour nos clients. Nous croyons fermement
                    que la technologie peut améliorer chaque aspect de
                    ces opérations
                </p>
            </div>

        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            years: [2018, 2019, 2020, 2021, 2022, 2023, 2024],
            selectedYear: 2023,
            visibleMobileYears: [2022, 2023],
            visibleYears: [2022, 2023, 2024], // Années visibles
        };
    },
    computed: {
        isFirstYear() {
            return this.selectedYear === this.years[0];
        },
        isLastYear() {
            return this.selectedYear === this.years[this.years.length - 1];
        },
        visibleYears() {
                  const index = this.years.indexOf(this.selectedYear);
                  if (index === -1) return [];
                  return this.years.slice(Math.max(0, index - 1), Math.min(index + 2, this.years.length));
            },
    },
    methods: {
        selectYearAndScroll(year) {
            const currentIndex = this.years.indexOf(this.selectedYear);
            const yearIndex = this.years.indexOf(year);
            const direction = yearIndex > currentIndex ? 1 : -1;
            this.scrollYear(direction);
            this.selectedYear = year;
        },
        scrollYear(direction) {
            const currentIndex = this.years.indexOf(this.selectedYear);
            const newIndex = currentIndex + direction;
            if (newIndex >= 0 && newIndex < this.years.length) {
                this.selectedYear = this.years[newIndex];
                // Mettez à jour les années visibles
                this.visibleYears = this.years.slice(Math.max(0, newIndex - 1), Math.min(this.years.length, newIndex + 2));
            }
        },

        selectYear(year) {
            this.selectedYear = year;
        },
        scrollYear(direction) {
            const currentIndex = this.years.indexOf(this.selectedYear);
            const newIndex = currentIndex + direction;
            if (newIndex >= 0 && newIndex < this.years.length) {
                this.selectedYear = this.years[newIndex];
            }
        },
    },
};
</script>

<style scoped>
img {
    z-index: 2;
}

.btn {
    padding: 10px 10px;
    margin: 20px 20px;
    height: 120px;
    width: 120px;
    background-color: #3A73B7;
    color: #ffffff;
    font-size: 18px;
    border: none;
    cursor: pointer;
    transition: all 0.3s;
    border-radius: 100%;
    margin: 0;
    position: relative;
    z-index: 2;
    /* Place les boutons en avant-plan */
}

.active-btn {
    height: 150px;
    width: 150px;
    font-size: 28px;
    font-weight: 500;
}

.description {
    padding: 8px;
    text-align: center;
}

/* Ligne pour relier les boutons */
.line {
    position: absolute;
    width: 700px;
    /* Largeur de la ligne de 700px */
    height: 3px;
    background-color: #3A73B7;
    bottom: 70px;
    /* Position par rapport aux boutons */
    left: 50%;
    /* Centrez horizontalement la ligne */
    transform: translateX(-50%);
    /* Centrez horizontalement la ligne */
    z-index: 1;
    /* Place la ligne derrière les boutons */
}

/* Utilisez les classes de Tailwind CSS pour personnaliser davantage le style */
</style>
