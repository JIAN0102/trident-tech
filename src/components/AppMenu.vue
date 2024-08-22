<script setup>
import { ref } from "vue";

const menus = ref([
  {
    id: "characteristic",
    title: "白頭翁的特性",
  },
  {
    id: "story",
    title: "白頭翁的故事",
  },
  {
    id: "photo",
    title: "白頭翁的美照",
  },
  {
    id: "crisis",
    title: "白頭翁的危機",
  },
]);

const activeMenuId = ref("");
const handleClickMenu = (id) => {
  if (id === activeMenuId.value) {
    activeMenuId.value = "";
    return;
  }
  activeMenuId.value = id;
};
</script>

<template>
  <nav>
    <ul class="space-y-[22px] text-center text-lg">
      <li v-for="menu in menus" :id="menu.id">
        <a
          href="javascript:;"
          class="border-b-2"
          :class="
            activeMenuId === menu.id
              ? 'border-[#aa6666] text-[#aa6666]'
              : 'border-transparent'
          "
          @click="handleClickMenu(menu.id)"
        >
          {{ menu.title }}
        </a>
      </li>
    </ul>
  </nav>
</template>
