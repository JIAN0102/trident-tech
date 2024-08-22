<script setup>
import { ref } from "vue";
import AppMenu from "@/components/AppMenu.vue";
import BaseLogo from "@/components/BaseLogo.vue";

const isMenuOpen = ref(false);
const handleToggleMenuOpen = () => {
  isMenuOpen.value = !isMenuOpen.value;
};
</script>

<template>
  <header class="relative z-50 shadow-[0_4px_4px] shadow-black/25 lg:hidden">
    <div class="flex items-center justify-between py-5 pl-[26px] pr-[18px]">
      <div class="w-10">
        <button
          type="button"
          class="relative block h-[22px] w-6"
          @click="handleToggleMenuOpen"
        >
          <span
            class="absolute h-1 w-full bg-black duration-300"
            :class="
              isMenuOpen
                ? 'left-1/2 top-1/2 -translate-x-1/2 -translate-y-1/2 -rotate-45'
                : 'left-0 top-0'
            "
          ></span>
          <span
            class="absolute left-0 top-[9px] h-1 w-4 bg-black duration-300"
            :class="{
              'translate-x-full opacity-0': isMenuOpen,
            }"
          ></span>
          <span
            class="absolute h-1 w-full bg-black duration-300"
            :class="
              isMenuOpen
                ? 'left-1/2 top-1/2 -translate-x-1/2 -translate-y-1/2 rotate-45'
                : 'left-0 top-[18px]'
            "
          ></span>
        </button>
      </div>
      <a href="javascript:;" class="text-xl font-bold">白頭翁不吃小米</a>
      <BaseLogo :size="48" />
    </div>

    <div v-show="isMenuOpen" class="px-[26px] pb-[45px] pt-1">
      <AppMenu />
    </div>
  </header>
</template>
