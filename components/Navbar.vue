<script setup>
import { BellIcon, MenuIcon, XIcon } from "@heroicons/vue/outline";
import trello from "@/assets/svg/Trello.svg?url";

const showShadow = ref(false);
onMounted(() => window.addEventListener("scroll", handleScroll));

const handleScroll = (e) => {
  if (document.documentElement.scrollTop >= 10) {
    showShadow.value = true;
  } else {
    showShadow.value = false;
  }
};
</script>
<template>
  <div
    class="bg-white flex h-16 justify-between sticky top-0 duration-500"
    :class="[showShadow ? 'shadow-3xl' : 'shadow-none']"
  >
    <div class="flex-shrink-0 flex items-center px-6" @click="handleScroll()">
      <img class="h-5.5 object-contain" :src="trello" alt="Trello" />
    </div>
    <div class="flex items-stretch">
      <button class="bg-[#0066ff] text-white px-6 py-2 text-xl">
        Get Trello for free
      </button>
    </div>
  </div>
</template>
