<template>
    <div id="bgImg" class="w-full h-[300px] mt-20 pt-16">

        <div class="flex flex-col justify-center">
            <div class="flex flex-col py-3">
                <h2 class="text-white text-center text-[18px]">Abonnez-vous à Notre Newsletter</h2>
            </div>
            <div class="flex items-center justify-center ">
                <form>
                    <div class="flex flex-col rounded-lg overflow-hidden sm:flex-row">
                        <input
                            class="py-3 px-4 w-[350px] bg-blue-50 text-gray-800 border-blue-100 border-1 outline-none placeholder-gray-700 focus:bg-gray-100"
                            type="text" name="email" placeholder="Entrez votre adresse e-mail">
                        <button
                            class="py-3 px-4 bg-dgl-primary text-gray-100 font-semibold uppercase hover:bg-gray-600">S'abonner</button>
                    </div>
                </form>
            </div>

        </div>
    </div>
</template>

<script setup>

</script>
<style scoped>
#bgImg {
    background-image: url("./../public/newsletterImage.svg");
}
</style>