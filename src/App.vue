<script setup>
import AppHeader from "@/components/AppHeader.vue";
import AppSideMenu from "./components/AppSideMenu.vue";

const features = [
  {
    id: "appearance",
    title: "外觀",
    description:
      "白頭鵯體長約17到22公分，額至頭頂純黑色而富有光澤，兩眼上方至後枕白色，形成一白色枕環。耳羽後部有一白斑，此白環與白斑在黑色的頭部均極為醒目，老鳥的枕羽(後頭部)更潔白，所以又叫「白頭翁」。",
  },
  {
    id: "habitat",
    title: "棲地",
    description:
      "白頭翁和麻雀、綠繡眼合稱「城市三寶」，常成群出現在平原區灌木叢、丘陵樹林地帶，以及校園、公園、庭院、行道中的各種高高的電線與樹上。",
  },
  {
    id: "habit",
    title: "食性",
    description:
      "以果樹的漿果和種子為主食，並時常飛入果園偷吃果實，還會吃嫩葉嫩芽，尤其是胡蝶蘭的嫩葉嫩芽葉，偶爾啄食昆蟲。",
  },
];
</script>

<template>
  <AppHeader />

  <main class="lg:flex">
    <AppSideMenu />

    <section class="flex flex-1 flex-col">
      <div
        class="relative min-h-[400px] flex-1 bg-black bg-[url('/images/hero-mobile.png')] bg-cover bg-center lg:bg-[url('/images/hero-desktop.png')]"
      >
        <div
          class="absolute bottom-0 right-0 w-full px-[22px] py-6 text-right text-white lg:px-11 lg:py-9"
        >
          <h1 class="text-5xl font-bold">白頭翁 (Chinese bulbul)</h1>
          <p class="mt-3 text-lg leading-snug">
            又名白頭鵯。以果實、昆蟲為主食，無法消化小米、穀類。平均壽命約 8~10
            年。
          </p>
        </div>
      </div>
      <div
        class="bg-[#dcccbc] px-9 pb-[70px] pt-[50px] lg:px-[50px] lg:pb-[84px] lg:pt-[58px]"
      >
        <div class="grid grid-cols-1 gap-x-20 gap-y-[50px] xl:grid-cols-3">
          <div
            v-for="feature in features"
            :key="feature.id"
            class="flex items-start gap-x-[38px]"
          >
            <div class="relative">
              <h3 class="writing-mode-vertical-rl text-4xl font-bold">
                {{ feature.title }}
              </h3>
              <div
                class="absolute -bottom-3 -right-4 h-[25px] w-[25px] rounded-full border-[8px] border-[#aa6666] border-opacity-60"
              ></div>
            </div>
            <p class="flex-1 leading-snug">
              {{ feature.description }}
            </p>
          </div>
        </div>
      </div>
    </section>
  </main>
</template>
