<template>
    <div>
        <div class="flex items-end w-full  bg-white">

            <footer class="w-full text--[#555151] bg-[#F5FEFD] body-font">
                <div
                    class="container flex flex-col flex-wrap px-5 py-12 mx-auto md:items-center lg:items-start md:flex-row md:flex-no-wrap">
                    <div class="flex-shrink-0 w-56 mx-auto text-center md:mx-0 md:text-left">
                        <a class="flex items-center justify-center md:justify-start cursor-pointer">
                            <img src="./../public/LOGO DGLGROUP-02.svg">
                        </a>
                    </div>
                    <div class="flex flex-wrap flex-grow mt-10 -mb-10 text-center md:pl-20 md:mt-0 md:text-left">
                        <div class="w-full px-4 lg:w-1/3 md:w-1/2">
                            <h2 class="mb-5 text-[24px] text-dm font-medium tracking-widest text-dgl-primary title-font">
                                Services
                            </h2>
                            <nav class="mb-10 list-none">
                                <li class="mt-3">
                                    <a
                                        class="text-[#555151] text-dm text-[20px] cursor-pointer hover:text-dgl-primary">Import</a>
                                </li>
                                <li class="mt-2">
                                    <a
                                        class="text-[#555151] text-dm text-[20px] cursor-pointer hover:text-dgl-primary">Export</a>
                                </li>
                                <li class="mt-2">
                                    <a
                                        class="text-[#555151] text-dm text-[20px] cursor-pointer hover:text-dgl-primary">Transport</a>
                                </li>
                            </nav>
                        </div>
                        <div class="w-full px-4 lg:w-1/3 md:w-1/2">
                            <h2 class="mb-5 text-[24px] text-dm font-medium tracking-widest text-dgl-primary title-font">
                                Explorer
                            </h2>
                            <nav class="mb-10 list-none">
                                <li class="mt-3">
                                    <a
                                        class="text-[#555151] text-dm text-[20px] cursor-pointer hover:text-dgl-primary">Accueil</a>
                                </li>
                                <li class="mt-2">
                                    <a class="text-[#555151] text-dm text-[20px] cursor-pointer hover:text-dgl-primary">A
                                        propos</a>
                                </li>
                                <li class="mt-2">
                                    <a
                                        class="text-[#555151] text-dm text-[20px] cursor-pointer hover:text-dgl-primary">Produits</a>
                                </li>
                                <li class="mt-2">
                                    <a
                                        class="text-[#555151] text-dm text-[20px] cursor-pointer hover:text-dgl-primary">Blog</a>
                                </li>
                            </nav>
                        </div>
                        <div class="w-full px-4 lg:w-1/3 md:w-1/2">
                            <h2 class="mb-5 text-[24px] text-dm font-medium tracking-widest text-dgl-primary title-font">
                                Contact
                            </h2>
                            <form class="mb-10 list-none sm:mx-auto ">
                                <input type="text" placeholder="Email"
                                    class=" h-[42px] p-4 mb-4 w-[280px] rounded-[33px] border-[1px]  border-blue-200 focus:border-blue-300">

                                <button
                                    class="flex bg-dgl-primary hover:bg-dgl-hover text-[16px] text-white font-inter py-[10px] px-[15px] rounded-full focus:outline-none focus:ring-2 focus:bg-dgl-primary focus:border-transparent transition duration-300 ">
                                    <a href="#" class="pr-[20px]">
                                        S'inscrire
                                    </a>
                                    <img src="./../public/octicon_arrow-right-16.svg" alt="" class="">
                                </button>
                            </form>

                        </div>

                    </div>
                </div>
                <div class=" hidden md:block bg-dgl-primary">
                    <div class="flex items-center container pl-16 py-4 mx-auto">
                        <div class="mr-[450px]">
                            <NuxtLink to="/">
                                <div class="cursor-pointer ">
                                    <img src="./../public/group.svg" alt="" />
                                </div>
                            </NuxtLink>
                        </div>


                        <div class="flex items-center space-x-6">
                            <div class="flex items-center space-x-2">
                                <div>
                                    <img src="./../public/call.svg">
                                </div>
                                <div class="text-white">+229 96 24 97 17</div>
                            </div>
                            <div class="flex items-center space-x-2">
                                <div>
                                    <img src="./../public/email.svg">
                                </div>
                                <div class="text-white">dgl@gmail.com</div>
                            </div>
                            <div class="flex items-center space-x-2">
                                <div>
                                    <img src="./../public/location_on.svg">
                                </div>
                                <div class="text-white">Bénin Agla Hlazounto C/3194 </div>
                            </div>
                        </div>
                    </div>
                </div>
            </footer>

        </div>

    </div>
</template>
