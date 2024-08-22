<script setup>
import AppMenu from "@/components/AppMenu.vue";
import BaseLogo from "@/components/BaseLogo.vue";
</script>

<template>
  <aside
    class="relative z-50 hidden min-h-screen w-[345px] bg-white px-12 py-[78px] text-center lg:block"
  >
    <div class="absolute right-0 top-12 translate-x-1/2">
      <BaseLogo />
    </div>
    <a href="javascript:;" class="text-3xl font-bold">白頭翁不吃小米</a>
    <div class="mt-[75px]">
      <AppMenu />
    </div>
  </aside>
</template>
