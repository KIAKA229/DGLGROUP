<template>
    <div class="bg-local h-[650px] w-full md:bg-fixed flex flex-col justify-center items-center ">
        <h2 class="text-white font-inter text-bold text-[30px]">Contactez-nous</h2>
        <form class="flex flex-col justify-center items-center my-6">
            <input type="text" placeholder="Nom"
                class="placeholder-black my-4 pl-6 h-[64px] w-[586px] rounded-[40px] border border-blue-100 focus:border-dgl-primary">
            <input type="text" placeholder="Email"
                class="placeholder-black my-4 pl-6 h-[64px] w-[586px] rounded-[40px] border border-blue-100 focus:border-dgl-primary ">

            <textarea
                class="placeholder-black pt-4 pl-6 my-4 h-[150px] w-[586px] rounded-[20px] border border-blue-100 focus:border-dgl-primary"
                placeholder="Message"></textarea>

        </form>
        <button
            class="flex bg-dgl-primary hover:bg-dgl-hover  text-[18px] text-white font-inter py-[12px] px-[20px] rounded-full transition duration-300">
            <NuxtLink to="/contact" class="pr-[20px]">
                Soumettre
            </NuxtLink>
            <img src="./../public/octicon_arrow-right-16.svg" alt="" class="">
        </button>
    </div>
</template>

<script setup>

</script>

<style lang="css" scoped>
div {
    background-image: url('./../public/backContact.svg');
    background-attachment: scroll;
}
</style>