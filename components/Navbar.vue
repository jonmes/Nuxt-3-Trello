<script setup>
import { BellIcon, MenuIcon, XIcon } from "@heroicons/vue/outline";
import trello from "@/assets/svg/Trello.svg?url";

onMounted(() => {
  window.addEventListener("click", console.log("click "));
});

const handleScroll = () => {
  console.log("hel scroll");
};
</script>
<template>
  <div class="bg-white flex h-16 justify-between sticky top-0">
    <div class="flex-shrink-0 flex items-center px-6" @click="handleScroll()">
      <img class="h-5.5 object-contain" :src="trello" alt="Trello" />
    </div>
    <div class="flex items-stretch">
      <button class="bg-[#0066ff] text-white px-6 py-2 text-xl" @click="handleScroll">
        Get Trello for free
      </button>
    </div>
  </div>
</template>
