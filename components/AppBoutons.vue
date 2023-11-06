<template>
  <div>
    <NuxtLink to="/contact" class="">
      <button
        class="flex bg-dgl-primary hover:bg-dgl-hover  text-[16px] text-white font-inter py-[8px] px-[10px] rounded-full transition duration-300">

        <slot></slot>

        <img src="./../public/octicon_arrow-right-16.svg" alt="" class="pl-2">
      </button>
    </NuxtLink>
  </div>
</template>