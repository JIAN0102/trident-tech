<script setup>
defineProps({
  size: {
    type: Number,
    default: 96,
  },
});
</script>

<template>
  <div
    class="relative rounded-full bg-white shadow-[0_0_6px] shadow-black/25"
    :style="{
      width: `${size}px`,
      height: `${size}px`,
    }"
  >
    <div
      class="absolute left-1/2 top-1/2 h-[41.66%] w-[45.83%] -translate-x-1/2 -translate-y-1/2 rounded-[160%_75%_95%_0] bg-black"
    ></div>
    <div
      class="absolute left-1/2 top-1/2 z-10 h-[29.16%] w-[45.83%] -translate-x-1/2 -translate-y-1/2 rounded-[70%_30%_25%_0] bg-white"
    ></div>
    <div
      class="absolute left-[55%] top-1/2 z-20 h-[8.33%] w-[8.33%] -translate-y-1/2 rounded-[50%] bg-black"
    ></div>
    <div
      class="absolute left-[55%] top-[43%] h-[12.5%] w-[31.25%] -rotate-[15deg] rounded-[0_100%_0_0] bg-black"
    ></div>
  </div>
</template>
