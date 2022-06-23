<script setup lang="ts">
type Theme = "light" | "dark";

const setColorTheme = (newTheme) => {
  useColorMode().preference = newTheme;
};
</script>
<template>
  <div class="min-h-screen bg-green-100 dark:bg-gray-700">
    <h1 class="dark:text-white text-black text-8xl">Hello</h1>
    <button
      @click="
        setColorTheme($colorMode.preference === 'dark' ? 'light' : 'dark')
      "
    >
      Toogle DarkMode
    </button>
  </div>
</template>

<style lang="scss" scoped></style>
